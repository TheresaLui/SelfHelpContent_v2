<properties
	  pageTitle="Check the amount of data on each physical partition"
	  description="Check the amount of data on each physical partition"
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
	  articleId="f2ab3221-b82d-402a-ace3-1aa31037dc8c"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check the amount of data on each physical partition

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** This query shows the amount of storage in GB used for each physical partition. 

[Query link](https://cdbsupport.kusto.windows.net/Support?query=H4sIAAAAAAAEAHWQwW7CMBBE75HyDytOoYUGqvaYSimlKIdUFMIHbJwViWR7I9sIqPrxdUKBHsrJHs%2fuyG9W1LJxnzt2%2bJyHwTfsazIERZbP10WaL%2bElAdxyNK2HV3chuUT5hg5LtJQKwTvtPlARJMlAsFVsx4qcaYQdV6R40K3anVJomi%2bCHA8z1l5TtXZscEuZXrxCAgoPkTc31j%2fd%2b0umKzqpYRxNJ49PD5PJ3e85HEHhPy1TKXl%2fI6jH%2bmcVyiMs0bjGNayzagRnlI7hqlaNt2YsJYlu8GRedW9figqDOIY5ivpvMhhqDVnSzsIU2vpoG4ES2vNE1wsdHOkK3g32qRtLlSe4VVJ8izoMfgCLndYaywEAAA%3d%3d&web=0)

```
ReportQuota5M
| where TIMESTAMP >= ago(1h)
| where GlobalDatabaseAccountName =="xxxxxxxxxxxx"
| summarize MaxConsumedStorageInGB = max(MaxUsage+MaxIndexUsage)/(1024.00*1024.00), TotalAllowedStorageInGB = max(MaxQuota)/(1024.00*1024.00) by PartitionId, DatabaseName, DatabaseRid, CollectionName, CollectionRid, TIMESTAMP
// Each PartitionId represents 1 physical partition
| extend FractionUsed =  MaxConsumedStorageInGB / TotalAllowedStorageInGB
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query, you can share the output table but make sure to not incude any internal information.

<!--/issueDescription-->

