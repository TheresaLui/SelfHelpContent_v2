<properties
	  pageTitle="Check Connection Debug ralative TSGs"
	  description="Check Connection Debug ralative TSGs"
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
	  articleId="dc1015c6-2635-44ca-a3c1-f7962148204d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check Connection Debug ralative TSGs

If the customer is facing issues related to connecting to Cosmos DB (Mongo API support) account endpoint, then please follow this document to get further information from the customer without delay before starting investigation.

<br>

**Related TSG:** Find additional Details at the [PG TSG 914: TransportException](https://cosmosdbdocs.azurewebsites.net/tsg/tsg914.html)   
Describes how to decode Microsoft.Azure.Documents.TransportException when debugging customer issues. The .NET direct/TCP transport stack, also known as "RNTBD" (Real Name To Be Determined) throws exceptions of this type. Exceptions contain a substantial amount of context information.

See Link [Transport Error Codes](https://cosmosdbdocs.azurewebsites.net/tsg/tsg914.html?q=Connectionrefused#transport-error-codes)
- ConnectFailed
- SslNegotiationFailed
- SendFailed
- ReceiveFailed
- ReceiveStreamClosed
- ChannelMultiplexerClosed
- DnsResolutionFailed

<br>

See Link [Transport Timeouts](https://cosmosdbdocs.azurewebsites.net/tsg/tsg914.html?q=Connectionrefused#timeouts)
- ConnectTimeout
- SslNegotiationTimeout
- SendLockTimeout
- SendTimeout
- ReceiveTimeout
- DnsResolutionTimeout
- ChannelOpenTimeout
- TransportNegotiationTimeout
- RequestTimeout

<br>

##Please make sure customer understands the following


```  
Cosmos DB is a multi-tenant service

Mongo client drivers use connection pooling.
Whenever a mongo client is initialized to a remote address, the driver establishes more than one connection.
One of the connections is used to send regular periodic commands like isMaster, ping.


The other connections are used to issue user commands like query/insert/delete.

It is possible that some of the connections in the connection pool to timeout (if that connection was not picked by driver to issue user commands for sometime).

Because, Cosmos DB is a multi tenant service and we tear down TCP connections which are not used for some time.

But, in such cases the driver automatically reconnects and issues the commands.

Hence unless customer see actual request failures (in this case, if the query failed) ? it means, the client driver auto reconnected and the requests succeeded.
```


<br>
<br>


##Collect Actionable information from Customer

Please request for the following details without any delay to help aid fast investigation:

1. Repro script that customer is using to reliably reproduce the issue
2. Actual client logs for failed operation
3. Timestamp or time range when the failure happened
4. If customer is unable to issue requests to the account please run the below commands based on their environment and provide the results (for both port 10250 and 10255):  
??a. On Windows 8/Win 2012 and later (only if the customer does not want to install  
b. Powershell Test-NetConnection -ComputerName <accountName>.documents.azure.com -Port 10250 -InformationLevel Detailed

