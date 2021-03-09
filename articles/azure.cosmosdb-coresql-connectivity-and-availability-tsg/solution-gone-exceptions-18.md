<properties
	  pageTitle="Gone exceptions"
	  description="Gone exceptions"
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
	  articleId="03a06c1b-8a01-41b0-9294-d208172da762"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Gone exceptions

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 

1\) For Timeout issues check max time during error scenarios
```
BackendEndRequest5M
| where TIMESTAMP > datetime(2019-06-12T12:27:34.7982646Z) and TIMESTAMP  < datetime(2019-06-12T19:57:34.7982646Z)
//| where Tenant =="cdb-ms-prod-eastus1-fd17" and PartitionId =="a536932e-57c6-48c6-86ed-eade0d8606ff" and ReplicaId =="131982632893492061"
| where CollectionRid =="Rp1qAMFWskY=" and DatabaseRid =="Rp1qAA==" 
| summarize percentile( MaxTimeMilliseconds/10000.0,99) by bin(TIMESTAMP,5m), tostring(StatusCode)
| render timechart
```

Also, check the server CPU usage using the below Kusto query
```
NodeCounter5MRoleInstanceEvent
| where TIMESTAMP > datetime(2019-06-12T12:27:34.7982646Z) and TIMESTAMP  < datetime(2019-06-12T19:57:34.7982646Z)
| where Tenant =="cdb-ms-prod-eastus1-fd17" and RoleInstance =="ServerCluster0_IN_91" //and PartitionId =="a536932e-57c6-48c6-86ed-eade0d8606ff" and ReplicaId =="131982632893492061"
| where CounterName ==@"\Processor(_Total)\% Processor Time"
| project TIMESTAMP, AverageCounterValue
| render timechart
```

2\) Please inform customer about your findings.

<!--/issueDescription-->

