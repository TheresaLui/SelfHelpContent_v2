<properties
	  pageTitle="Server Side issue Troubleshooting"
	  description="Server Side issue Troubleshooting"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="748efef5-6b7b-4be3-8b39-8c38a592b7fd"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Server Side issue Troubleshooting

While the customer gathers client-side information, we can also **rule out server side issues**.

# ServiceUnavailable
ServiceUnavailable mostly happens when the SDK had timeouts, retried, and eventually gave up, so it could potentially be a case of just timeouts (see below steps).
But there has been cases where the ServiceUnavailable (503) comes **from Gateway** (through an HTTP Request).

For example:
```
Microsoft.Azure.Documents.DocumentClientException: Service is currently unavailable. More info: https://aka.ms/cosmosdb-tsg-service-unavailable
ActivityId: 88267ceb-1270-4e69-8a11-da2b484df2ea, Microsoft.Azure.Documents.Common/2.11.0, documentdb-dotnet-sdk/2.1.3 Host/64-bit MicrosoftWindowsNT/6.2.9200.0
   at Microsoft.Azure.Documents.Client.ClientExtensions.<ParseResponseAsync>d__1.MoveNext()
```

The part where it says `ClientExtensions.<ParseResponseAsync>` is actually a hint that this came from the backend.
One easy way to rule this out is, **find the ActivityId**, and check it in FrontendEvent:
```
FrontendEvent
| where ActivityId == "88267ceb-1270-4e69-8a11-da2b484df2ea"
```

```
EventName="FormattedMessageEvent" FormattedMessage="DocumentClientException with status code {0}, message: {1}, inner exception: {2}, and response headers: {3}" Argument0="ServiceUnavailable" Argument1="Service is currently unavailable. More info: https://aka.ms/cosmosdb-tsg-service-unavailable" Argument2="Microsoft.Azure.Documents.GoneException: The requested resource is no longer available at the server.
ActivityId: 88267ceb-1270-4e69-8a11-da2b484df2ea, Request URI: /7e2a44fa-1170-4fb6-b36e-7e8459abb82e/7c8f7111-96e3-4afd-9671-56a2cda84af8, RequestStats: , SDK: Microsoft.Azure.Documents.Common/2.11.0 ---> System.TimeoutException: Operation timed out. ---> System.Runtime.InteropServices.COMException: Exception from HRESULT: 0x80071BFF
   at System.Fabric.Interop.NativeClient.IFabricServiceManagementClient6.EndResolveServicePartition(IFabricAsyncOperationContext context)
   at System.Fabric.FabricClient.ServiceManagementClient.ResolveServicePartitionEndWrapper(IFabricAsyncOperationContext context)
   at System.Fabric.Interop.AsyncCallOutAdapter2`1.Finish(IFabricAsyncOperationContext context, Boolean ....
```

In this case, the error is a **Fabric timeout**.

If you find a record and there is mention of **TransportException** (or the original error from the user mentions TransportException), skip ahead to the [TransportException section](#transportexception-(.net)).

If you find a record, and there is **no TransportException**, you can follow [TSG: Availability - Unavailable](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/237408/) for more information and contact **Control Plane**.

If you don't find a record or the exception stack shows that there were TCP timeouts involved, follow the next couple of points.

# HTTP timeouts (.NET)
.NET uses the `System.Net.HttpClient` to do HTTP requests. This client whenever it runs into a timeout, it will surface this as a `TaskCanceledException` or `OperationCanceledException`.

For example (notice the `System.Net.Http` in the stack):
```
Microsoft.Azure.Cosmos.CosmosException : Response status code does not indicate success: InternalServerError (500); Substatus: 0; ActivityId: 00000000-0000-0000-0000-000000000000; Reason: (The operation was canceled.);
 ---> System.Threading.Tasks.TaskCanceledException: The operation was canceled.
   at System.Net.Http.ConnectHelper.ConnectAsync(String host, Int32 port, CancellationToken cancellationToken)
   at System.Net.Http.HttpConnectionPool.ConnectAsync(HttpRequestMessage request, Boolean allowHttp2, CancellationToken cancellationToken)
   at System.Net.Http.HttpConnectionPool.CreateHttp11ConnectionAsync(HttpRequestMessage request, CancellationToken cancellationToken)
   at System.Net.Http.HttpConnectionPool.GetHttpConnectionAsync(HttpRequestMessage request, CancellationToken cancellationToken)
   at System.Net.Http.HttpConnectionPool.SendWithRetryAsync(HttpRequestMessage request, Boolean doRequestAuth, CancellationToken cancellationToken)
   at System.Net.Http.RedirectHandler.SendAsync(HttpRequestMessage request, CancellationToken cancellationToken)
   at System.Net.Http.DiagnosticsHandler.SendAsync(HttpRequestMessage request, CancellationToken cancellationToken)
   at Microsoft.Azure.Cosmos.DocumentClient.HttpRequestMessageHandler.SendAsync(HttpRequestMessage request, CancellationToken cancellationToken)
```

These timeouts can happen for three reasons: 
1. Gateway is indeed having a long response time that exceeds the SDK request timeout (65 seconds by default, but the user can be changing it).
* For V3 .NET SDK, [CosmosClientOptions.RequestTimeout](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmos.cosmosclientoptions.requesttimeout).
* For V2 .NET SDK, [ConnectionPolicy.RequestTimeout](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.requesttimeout)
2. Gateway is down on the federation.
3. There is a [client-side connectivity issue](https://docs.microsoft.com/en-us/azure/cosmos-db/troubleshoot-dot-net-sdk-request-timeout).

The **first case** can be identified by doing the following:

1. Check the max latency on Gateway around the time of the incident:
```
Request5M
| where globalDatabaseAccountName == "<account-name>"
| where TIMESTAMP > ago(1d) // Adjust based on time of incident
| summarize max(MaxTimeMilliseconds) by bin(TIMESTAMP, 5m), verb, category
```
If you see the operations taking longer than the timeout (for example, a Delete collection operation would be verb DELETE, category Collection), then **contact or transfer to Control Plane** to understand why these operations are taking longer than the expected 65 seconds.

The **second case** can be identified by doing the following:
1. Check the Gateway activity on the account, can you see requests landing in the last 30 minutes?
```
Request5M
| where globalDatabaseAccountName == "<account-name>"
| where TIMESTAMP > ago(30m)
| distinct Tenant, RoleInstance
```
2. If no activity is found, do you see some activity going further in time? If yes, take note of the **Tenant and RoleInstance**.
3. Do you see *any* activity for that Tenant in the past 30 minutes?
```
Request5M
| where Tenant == "<tenant>"
| where TIMESTAMP > ago(30m)
| count 
```
4. If no activity is found, check the health in the [CosmosDB Dashboard](https://cosmosdbdashboard.cloudapp.net/WinFab/WinFabExplorer.aspx) for the Tenant, and see what's the health of Gateway Application, if it's Error / Warning, **contact Availability & Store Sev2/3 (depending on current incident level) or Control Plane**.

# TransportException (.NET)
If the stack trace contains a **TransportException** it means it's a TCP request failing (client on Direct/TCP mode).

To understand **why the exception happen**, see [TSG 914](https://cosmosdbdocs.azurewebsites.net/tsg/tsg914.html), that has explanations of all possible error codes and reasons (in case user is asking what is happening), plus also extra information on the exception.
This could be a client-side issue (hence why we start with the client-side investigation) OR it could be a **health problem in the replica**.

## CPU History
One **easy rule-out is CPU**, the TransportException has a **CPU History** that shows information like:
```
CPU history: 
(2020-08-28T00:40:09.1769900Z 0.114), 
(2020-08-28T00:40:19.1763818Z 1.732), 
(2020-08-28T00:40:29.1759235Z 0.000), 
(2020-08-28T00:40:39.1763208Z 0.063), 
(2020-08-28T00:40:49.1767057Z 0.648), 
(2020-08-28T00:40:59.1689401Z 0.137), 
CPU count: 8)
```

If you see values > 80% it would mean there was a CPU spike, or the time between the measurements is higher than 10 seconds, it means there was **thread starvation** on the client. Both should be followed with the customer telling them about the metrics and their meaning, and they should be checking if CPU is always high or if the machines need to be scaled up.

## Private endpoints
If the `rntbd` address contains the Account Name (instead of a Tenant), then it means the user is using Private Endpoints. For example:

```
rntbd://prod-panther-wakanda-southcentralus.documents.azure.com:1919/apps/25f852a5-ad54-43c7-93bc-cbf32baee5fb/services/ad9f84d2-9c44-487c-a1ad-fd5c0a349f1d/partitions/46fbddbc-8235-46a2-a236-0fa8afd17abe/replicas/132457908071454844p/, LSN: -1, GlobalCommittedLsn: -1, PartitionKeyRangeId: , IsValid: False, StatusCode: 410, SubStatusCode: 0, RequestCharge: 0, ItemLSN: -1, SessionToken: , UsingLocalLSN: False, TransportException: A client transport error occurred: The connection attempt timed out. 
```

In this case, contact or transfer to **Transport queue**, they would be the ideal team to troubleshoot Private endpoint connectivity (the RNTBD endpoint does not show which is the tenant or port so you cannot check the Replica health easily).

## Replica health
To rule out the replica health, follow [TSG 913](https://cosmosdbdocs.azurewebsites.net/tsg/tsg913.html), the Kusto queries there cover scenarios where you will end up transferring to Availability queue or Transport queue if they are positive.

If CPU health is fine, Replica health is fine, and user is not running into connection limiting (for example, no SNAT port exhaustion), **contact Transport queue** as the TCP connectivity is not owned by SDK team.

# Verification of in-progress Package/App Upgrade (Direct mode)
There is a chance that a client-side timeout might occur when the client is trying to connect to the address of a replica that it's being affected by a **package/app upgrade**.
To validate this, first obtain from the customer any Diagnostics logs that would show which is the federation involved, for example:

### Java
```
RequestStartTime: "20 Aug 2020 02:30:06.091", RequestEndTime: "20 Aug 2020 02:30:07.127", Duration: 1036 ms, Number of regions attempted: 1 StoreResponseStatistics{requestResponseTime="20 Aug 2020 02:30:07.105", 
storeResult=storePhysicalAddress: null, lsn: -1, globalCommittedLsn: -1, partitionKeyRangeId: null, isValid: false, statusCode: 410, subStatusCode: 0, isGone: true, isNotFound: false, isInvalidPartition: false, requestCharge: 0.0, itemLSN: -1, sessionToken: null, 
exception: failed to establish connection to cdb-ms-prod-westus1-fd38.documents.azure.com:14147: connection timed out: cdb-ms-prod-westus1-fd38.documents.azure.com/40.112.241.37:14147, requestResourceType=Document, requestOperationType=Read} 
```

### .NET
More or less the exception will have the following:
```
ResponseTime: 2020-07-16T09:27:11.1965966Z, 
StoreResult: StorePhysicalAddress: rntbd://cdb-ms-prod-westus1-fd38.documents.azure.com:14147/apps/7b364811-e427-44a1-beb4-0c4cd7e12dd5/services/63861cf5-e181-4fee-8712-3cd1b167ffc7/partitions/fd8b5f87-d7c1-413f-906a-389e356d9deb/replicas/132375317683992325s/, 
LSN: -1, GlobalCommittedLsn: -1, PartitionKeyRangeId: , IsValid: False, 
StatusCode: 410, SubStatusCode: 0, RequestCharge: 0, ItemLSN: -1, SessionToken: , UsingLocalLSN: True, 
TransportException: A client transport error occurred: Acquiring the send stream lock timed out. (Time: 2020-07-16T09:27:11.1965966Z, activity ID: 45bd5beb-c6d9-4943-becf-34a2c4e4c33e, error code: SendLockTimeout [0x000D], base error: HRESULT 0x80131500, URI: 
```

We can see from that Diagnostics that the affected federation was **cdb-ms-prod-westus1-fd38.documents.azure.com:14147**

First we can run this **Kusto query**, **replacing the name, port, and adjusting TIMESTAMP range**:

```
InstanceEndpointHealthEventG
| where Tenant == "cdb-ms-prod-westus1-fd38"
| where TIMESTAMP > now(-24h)
| where port == 14147
| summarize count() by health, bin(TIMESTAMP, 5m)
| render timechart 
```

If there is a dip in the health that matches the time where the user is seeing the timeouts, it could potentially be the source.

## Is the issue ongoing?
The next step is to verify through the Deployment Status: https://cosmosdbdashboard.cloudapp.net/CosmosX/DeploymentStatus.aspx

If filtering by the region shows the orange Package/App Upgrade status, it means the federation is definitively ongoing upgrade and this might impact connectivity:

## Is the issue in the past?
If this incident is not ongoing, but something that happened in the past (RCA), another alternative is checking this **Kusto query**:
```
https://dataexplorer.azure.com/clusters/cdbsupport/databases/Support?query=H4sIAAAAAAAAA3PMyQktSC9KTEkt1lBKTknSzS3WLSjKT9EtTy0uKS021E1LMVbSBABWVRjoJgAAAA==

AllUpgrades("cdb-ms-prod-westus1-fd3")
```

The results contain a table where it can be verified by time range if there was any upgrade:

