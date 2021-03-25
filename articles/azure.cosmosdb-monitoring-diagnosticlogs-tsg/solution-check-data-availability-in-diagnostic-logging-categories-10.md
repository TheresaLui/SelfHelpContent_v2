<properties
	  pageTitle="Check Data Availability in Diagnostic Logging Categories"
	  description="Check Data Availability in Diagnostic Logging Categories"
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
	  articleId="96a0101e-95b3-4fa7-b709-30430f4b3017"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check Data Availability in Diagnostic Logging Categories

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Investigation (not customer message):**
This TSG is to identify the properties that are available per diagnostic log category.  The properties map to columns in AzureDiagnostics

### Azure CosmosDB Diagnostic Log overview
The logs are categorized into seven categories such as:  

- DataPlaneRequest
- QueryRuntimeStatistics
- PartitionKeyStatistics
- PartitionKeyRUConsumption
- MongoRequests
- CassandraRequests
- ControlPlaneRequest

Each category emits different properties (i.e. Columns in AzureDiagnostics).  There are several support tickets that customers ask why certain columns are empty for a category in AzureDiagnostics.

### DataPlaneRequest
#### Direct Mode
The following properties (i.e. Columns in AzureDiagnostics) are emitted for DataPlaneRequest in Direct mode.

https://msdata.visualstudio.com/CosmosDB/_git/CosmosDB?path=%2FProduct%2FCosmos%2FServiceMonitoring%2FConfigGen%2FWarmPathTemplates%2FDiagLogsWarmpathConfig_Template.xml&version=GBmaster&line=136&lineEnd=155&lineStartColumn=1&lineEndColumn=95&lineStyle=plain

          let ActivityIdProperty = Concat("","\"activityId\": \"", ActivityId)
          let UserAgentProperty = Concat( "","\",\"userAgent\": \"", UserAgent)
          let ResourceTypeProperty = Concat( "","\",\"requestResourceType\": \"", resourceType)
          let StatusCodeProperty = Concat( "","\",\"statusCode\": \"", StatusCode)
          let RequestResourceIdProperty = Concat("", "\",\"requestResourceId\": \"", ResourceId)
          let ClientIpAddressProperty = Concat( "","\",\"clientIpAddress\": \"", IpAddress)
          let RequestChargeProperty = Concat( "","\",\"requestCharge\": \"", RequestCharge)
          let CollectionRidProperty = Concat( "","\",\"collectionRid\": \"", CollectionRid)
          let DurationProperty = Concat( "","\",\"duration\": \"", (Duration/(10000)))
          let RequestLengthProperty = Concat( "","\",\"requestLength\": \"", RequestLength)
          let ResponseLengthProperty = Concat( "","\",\"responseLength\": \"", ResponseLength)
          let ResourceTokenUserRidProperty = Concat( "","\",\"resourceTokenUserRid\": \"", ResourceTokenUserRid)
          let RegionProperty = Concat( "","\",\"region\": \"", Region)
          let PartitionIdProperty = Concat( "","\",\"partitionId\": \"", PartitionId)
          let KeyTypeProperty = Concat( "","\",\"keyType\": \"", KeyType)
          let DatabaseNameProperty = Concat( "","\",\"databaseName\": \"", DatabaseName)
          let CollectionNameProperty = Concat( "","\",\"collectionName\": \"", CollectionName)
          let CallerIdProperty = Concat( "","\",\"callerId\": \"", CallerId)
          let TransportLayerSecurityProtocolProperty = Concat( "","\",\"transportLayerSecurityProtocol\": \"", TransportLayerSecurityProtocol)
          let ConnectionModeProperty = Concat( "","\",\"connectionMode\": \"", ConnectionMode)

#### Gateway Mode
The following properties are emitted for the DataPlaneRequest in Gateway mode.

https://msdata.visualstudio.com/CosmosDB/_git/CosmosDB?path=%2FProduct%2FCosmos%2FServiceMonitoring%2FConfigGen%2FWarmPathTemplates%2FDiagLogsWarmpathConfig_Template.xml&version=GBmaster&line=234&lineEnd=249&lineStartColumn=1&lineEndColumn=95&lineStyle=plain

          let ActivityIdProperty = Concat("","\"activityId\": \"", ActivityId)
          let UserAgentProperty = Concat( "","\",\"userAgent\": \"", userAgent)
          let ResourceTypeProperty = Concat( "","\",\"requestResourceType\": \"", resourceType)
          let StatusCodeProperty = Concat( "","\",\"statusCode\": \"", statusCode)
          let RequestResourceIdProperty = Concat("", "\",\"requestResourceId\": \"", uri)
          let ClientIpAddressProperty = Concat( "","\",\"clientIpAddress\": \"", address)
          let RequestChargeProperty = Concat( "","\",\"requestCharge\": \"", requestCharge)
          let CollectionRidProperty = Concat( "","\",\"collectionRid\": \"", collectionResourceId)
          let DatabaseRidProperty = Concat( "","\",\"databaseRid\": \"", databaseResourceId)
          let DurationProperty = Concat( "","\",\"duration\": \"", milliseconds)
          let RequestLengthProperty = Concat( "","\",\"requestLength\": \"", requestSize)
          let ResponseLengthProperty = Concat( "","\",\"responseLength\": \"", responseSize)
          let ResourceTokenUserRidProperty = Concat( "","\",\"resourceTokenUserRid\": \"", "")
          let RegionProperty = Concat( "","\",\"region\": \"", region)
          let PartitionIdProperty = Concat( "","\",\"partitionId\": \"", "")
          let ConnectionModeProperty = Concat( "","\",\"connectionMode\": \"", ConnectionMode)

### QueryRuntimeStatistics
The following properties are emitted for the QueryRuntimeStatistics

https://msdata.visualstudio.com/CosmosDB/_git/CosmosDB?path=%2FProduct%2FBackend%2Fnative%2Fqueryengines%2FqueryLanguages%2Fsql%2FQueryEngine.SqlQueryAsyncContext.cpp&version=GBmaster&line=528&lineEnd=532&lineStartColumn=11&lineEndColumn=40&lineStyle=plain

            L"{\"activityId\": \"%s\","
            L" \"databasename\": \"%s\","
            L" \"collectionname\": \"%s\","
            L" \"partitionkeyrangeid\": \"%s\","
            L" \"querytext\": \"%s\"}",


## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer.

<!--/issueDescription-->

