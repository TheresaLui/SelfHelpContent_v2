<properties
	  pageTitle="Issue Category"
	  description="Issue Category"
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
	  articleId="c6b0c31e-d395-4446-a5d2-22ad748feba4"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Issue Category

Customers may face variety of Availability issues such as:
1. DNS Resolution Failure
2. Availability SLA Violated
3. Gateway Mode Offline
4. Endpoint Offline
5. Java/.Net (Gone exceptions, Timeout, etc.)
</br>

1- Get the Database Account Name and review the Cosmos DB Account SLA </br>
2- Follow every step mentioned below.

## Step 1) Check if it is DNS Resolution Failure
1. Collect the Complete Error and Exceptions Stack
2. If the Error *"The remote name could not be resolved. Since, the issue is with networking and DNS"* then it is a DNS Resolution Issue

## Step 2) Check if Cosmos DB Availability SLA was violated
1. The Azure portal does show the Availability SLA for the given Account.  The customer should be able to check any availability issue in the portal to confirm any service issue. The Azure Portal basically uses the "ComsosDBAccountAvailability".
2. Metric to display the chart for customers which we can query through Jarvis: https://jarvis-west.dc.ad.msft.net/dashboard/DocumentDB/SLA. 
3. The availability is down if the chart show any drop.

**Example :** No SLA Violation - click in this [image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EXVVCueq0jJBjVkpVs_gyUsBZTt_p-V8T0fB1uwTnnR6Ew?e=5f4FK6).

## Step 3) Check if it is Gateway Mode
Ensure we get the complete Call Stack as show below. The class **"Microsoft.Azure.Documents.GatewayStoreModel"** indicates the connection is using **Gateway Mode**.  Also, you can get the connection mode from Customer.

```
Exception_ClassName_s        System.Threading.Tasks.TaskCanceledException Exception_Message_s        A task was canceled. Exception_StackTraceString_s        at System.Runtime.CompilerServices.TaskAwaiter.ThrowForNonSuccess(Task task
 at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task
 at Microsoft.Azure.Documents.GatewayStoreModel.<>c__DisplayClass20_0.<<InvokeAsync>b__0>d.MoveNext() --- End of stack trace from previous location where exception was thrown --
```

## Step 4) Check if Gateway Service is Online
1. Extract the Tenant Name using the [Jarvis](https://jarvis-west.dc.ad.msft.net/D16B267D)
   Update the Account Name
   Update the Time window for +- 1 hour

2. Review the Status using the CRUD Runner using [Jarvis](https://jarvis-west.dc.ad.msft.net/?page=logs&be=DGrep&time=2019-02-19T12%3A13%3A00.000Z&offset=~2&offsetUnit=Hours&UTC=true&ep=Diagnostics%20PROD&ns=RunnerService&en=RunnerCentralEventTable&serverQuery=where%20Status%20!%3D%20%22Healthy%22%20and%20Status%20!%3D%20%22Timeout%22%20and%20Name.Contains(%22DatabaseAccountCrudRunner%22)%20and%20(UserField1%20%3D%3D%20%22CRUDOperationFailed%22)&clientQuery=where%20RunnerInstance%3D%3D%22cdb-ms-prod-northeurope1-fd1%22&chartEditorVisible=true&chartType=Line&chartLayers=%5b%5b%22New%20Layer%22%2C%22%22%5d%5d%20).  
   a. Update the Time Range from the Exception  
   b. Add the Tenant Name in the Client Filter Section from Step 1  
   c. Run the Query and review the result as follows  
      i. **Zero Rows Returned**  - The Gateway Service is Online     
      ii. **Row Returned**  - The Gateway Service if Offline

See [image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/ETqYzbAjyIlMmrqUyQA77OEBK__ev1DZl5Zg2QMKr3mLxg?e=pT3y0j)

## Step 5) A. Check if Endpoint is Online

### NetworkConnectivityWatchdog

#### Overview
A NetworkConnectivityWatchdog now continuously monitors the health of each endpoint of master and server processes.  The NetworkConnectivityWatchdog  probes the endpoint in regular frequency as stated below. The watchdog log can be used to evaluate the status of the endpoint precisely.

There are two types of probes.

##### ConnectProber 
> Networkwatchdog  creates a new connection, negotiates SSL, sends a request and validates the response.

> It probes every 60 seconds

##### RequestProber
> Networkwatchdog uses the existing connection to send a request and validates the response

> It probes every 10 seconds

##### Total Count & Missing Count in below Kusto Queries.
> There are totally 70 counts for above 2 Prober in every 10 mins (600s): 600/60+600/10 = 70, so for +-10 mins (20 mins) it should be **140** in normal situation. And that's why MissingCount is calculated by 14 * IntervalInput / 1m = 140, to subtract total count.

**Probe Logs telemetry in the Kusto table InstanceEndpointHealthEventG**

#### How to check the Health status of the Endpoint

##### OPTION 1) If customer provided exception contains port number

> Extract timestamp, tenant, and port number. Run the following query.
```txt
let TimestampInput = datetime(<Timestamp>);
let IntervalInput = 10m;
let TenantInput = "<Tenant>";
let PortInput = <Port number>;
cluster('cdbsupport.kusto.windows.net').database('Support').InstanceEndpointHealthEventG
| where TIMESTAMP > TimestampInput - IntervalInput and TIMESTAMP < TimestampInput + IntervalInput
| where Tenant == TenantInput and port == PortInput
| summarize TotalCount = count(), UnhealthyCount = countif(health == "Unhealthy") by Tenant, RoleInstance, protocol, port
| extend MissingCount = 14 * IntervalInput / 1m - TotalCount
```
> ResponseTime: **2020-03-03T19:48:46.1449872Z**, StoreResult: StorePhysicalAddress: rntbd://**cdb-ms-prod-northcentralus1-fd7**.documents.azure.com:**14027**/apps/fdb1445f-aa81-4446-9a21-272892b7788a/services/7fd8fa7f-7db9-45a0-b7b6-f745fd2036ed/partitions/563e8457-1942-43eb-b6a8-9aebcb6c641e/replicas/132271431103880573p/, LSN: -1, GlobalCommittedLsn: -1, PartitionKeyRangeId: , IsValid: False, StatusCode: 410, SubStatusCode: 0, RequestCharge: 0, ItemLSN: -1, SessionToken: , UsingLocalLSN: False, TransportException: A client transport error occurred: SSL negotiation timed out. (Time: 2020-03-03T19:48:46.1449872Z, activity ID: 1ea43f80-3f24-40b4-97b3-bfa2f7d4ab67, error code: SslNegotiationTimeout [0x0008], base error: HRESULT 0x80131500, URI: rntbd://cdb-ms-prod-northcentralus1-fd7.documents.azure.com:14027/, connection: 10.0.0.32:54446 -> 52.162.106.10:14027, payload sent: False, CPU history: not available, CPU count: 40), ResourceType: Document, OperationType: Create

##### OPTION 2) If customer provided exception does not contain port number

> Extract timestamp, partition ID, and replica ID. Run the following query.
```txt
let TimestampInput = datetime(<Timestamp>);
let IntervalInput = 10m;
let PartitionIdInput = "<Partition ID>";
let ReplicaIdInput = "<Replica ID>";
Replica
| where TIMESTAMP > TimestampInput - 30m and TIMESTAMP < TimestampInput + 30m
| where PartitionId == PartitionIdInput and ReplicaId == ReplicaIdInput
| where Message startswith "ReplicaMetricReporter::ReportContext"
| summarize by Tenant, RoleInstance
| join kind = inner
(
    cluster('cdbsupport.kusto.windows.net').database('Support').InstanceEndpointHealthEventG
    | where TIMESTAMP > TimestampInput - IntervalInput and TIMESTAMP < TimestampInput + IntervalInput
)
on Tenant, RoleInstance
| summarize TotalCount = count(), UnhealthyCount = countif(health == "Unhealthy") by Tenant, RoleInstance, protocol, port
| extend MissingCount = 14 * IntervalInput / 1m - TotalCount
```

> "Error":"Message: Channel is closed\r\nActivityId: 33f4310c-bc30-4106-bc4f-a20fed82ea69, Request URI: /apps/274509a2-d536-4a09-b0a3-f4fd526feb25/services/93d47f05-a2cd-411d-992e-6ed60918b588/partitions/**83e62684-4c07-4acb-8a56-a3c0b9af37b8**/replicas/**132172720096843866**p/, RequestStats: \r\nRequestStartTime: **2020-03-03T15:35:15.8610967Z**, RequestEndTime: 2020-03-03T15:35:15.8610967Z, Number of regions attempted:1\r\n, SDK: Windows/10.0.14393 documentdb-netcore-sdk/2.9.2"}

##### OUTPUT 1) If MissingCount` and `UnhealthyCount` are both 0

> > It indicates that this port was heathy during that time. This is not a service transport issue and it could be network or client side issue.

##### OUTPUT 2) If `MissingCount` is greater than 1, 

> > It indicates an upgrade, high CPU, or monitoring issue on the service.  
> >
> > **Please engage engineering through CRI**

##### OUTPUT 3) If `UnhealthyCount` is greater than 1, 

> > It indicates that this port had some unavailability during this time. Please proceed to 
> > **Please engage engineering through CRI**
<br>

**Guidance to Customer for troubleshooting Client Side issue**
1.  If SDK < 2.3.2 and customer complains of service unavailable, we suggest upgrading SDK
2.  If the client CPU > 80% we point that as the root cause.
See [image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/ETqYzbAjyIlMmrqUyQA77OEBK__ev1DZl5Zg2QMKr3mLxg?e=qySWoJ)


## Step 6) (Java/.NET Only) Has the customer tried the public troubleshooting guide?

### Java Troubleshooting Guide

Have customer follow these steps: https://docs.microsoft.com/en-us/azure/cosmos-db/troubleshoot-java-async-sdk

If no, point it out to them that it can help them troubleshoot on their own in the future, but you can walk through the steps below.

**Is it failing across multiple backend clients at the same time?**   

 **If yes**. This is indicative of an issue not in the SDK, but between the SDK and the backend service. If you've checked for backend service issues, then it's worth looping in Azure Networking to look for a cause. Also ask whether they are using any Proxies/VNET firewall applicances/etc. that could cause issues.

 **If no**, check for issues in the client environment:
- Majority of our Client are getting the "Service Unavailable" Exception is due to High CPU on the Client Environment. Also, ensure the CPU usage are monitored in 5 second interval.  Anything greater than 5 seconds interval does not reveal High CPU usage.
- Small Subset of issue were due to Client Side Network Issue

**a.** No connections successful at all?
- Check local port firewalls - Direct requires a lot of opened Ports/IP Addresses to be exposed

**b.** Some failing at first, then more and more failing?
- SNAT issues - https://docs.microsoft.com/en-us/azure/cosmos-db/troubleshoot-dot-net-sdk#snat

**c.** Just intermittent connectivity issues
- Run 'netstat' and look for number of requests in TIME_WAIT state. Can indicate we're closing connections too much, which will exhaust the connection pool. Solution is to increase connection pool size (and file descriptors to make sure we can actually open more sockets) (or to scale out to limit requests per client sdk if they can't control connection pool size (like app service)).
- Tools to Suggest is to User Perfmon if its On-premise environment
- Engage the Azure respective services if the application is running in Azure Platform

## For Gone Exceptions, check if Role Instance is changing in below  query.. You will find partition Id, Tenant and replicaid in error stack

Example:

```
BackendEndRequest5M
| where TIMESTAMP > datetime(2019-06-12T12:27:34.7982646Z) and TIMESTAMP  < datetime(2019-06-12T19:57:34.7982646Z)
| where Tenant =="cdb-ms-prod-eastus1-fd17" and PartitionId =="a536932e-57c6-48c6-86ed-eade0d8606ff" and ReplicaId =="131982632893492061"
//| where CollectionRid =="Rp1qAMFWskY=" and DatabaseRid =="Rp1qAA=="
//| summarize sum(SampleCount) by bin(TIMESTAMP,5m), tostring(StatusCode)
//| render timechart
```

``
Service is currently unavailable. ActivityId: e7c991bd-0000-0000-0000-000000000000, RequestStartTime: 2019-06-11T14:48:35.3209968Z, RequestEndTime: 2019-06-11T14:51:04.7229171Z, Number of regions attempted: 1 ResponseTime: 2019-06-11T14:49:00.1413221Z, StoreResult: StorePhysicalAddress: rntbd://cdb-ms-prod-southcentralus1-fd4.documents.azure.com:14008/apps/f42249a5-7d70-4acb-9e00-6e5f344b92db/services/01d667c7-9386-472d-b79a-e671dececb5c/partitions/5d685886-60a3-42c3-9996-11d32205f120/replicas/132026475180646926s/,
``

## For Timeout issues Check max time during error scenarios

```
BackendEndRequest5M
| where TIMESTAMP > datetime(2019-06-12T12:27:34.7982646Z) and TIMESTAMP  < datetime(2019-06-12T19:57:34.7982646Z)
//| where Tenant =="cdb-ms-prod-eastus1-fd17" and PartitionId =="a536932e-57c6-48c6-86ed-eade0d8606ff" and ReplicaId =="131982632893492061"
| where CollectionRid =="Rp1qAMFWskY=" and DatabaseRid =="Rp1qAA==" 
| summarize percentile( MaxTimeMilliseconds/10000.0,99) by bin(TIMESTAMP,5m), tostring(StatusCode)
| render timechart
```

<br>

## Also, See the server CPU usage using below

```
NodeCounter5MRoleInstanceEvent
| where TIMESTAMP > datetime(2019-06-12T12:27:34.7982646Z) and TIMESTAMP  < datetime(2019-06-12T19:57:34.7982646Z)
| where Tenant =="cdb-ms-prod-eastus1-fd17" and RoleInstance =="ServerCluster0_IN_91" //and PartitionId =="a536932e-57c6-48c6-86ed-eade0d8606ff" and ReplicaId =="131982632893492061"
| where CounterName ==@"\Processor(_Total)\% Processor Time"
| project TIMESTAMP, AverageCounterValue
| render timechart
```

