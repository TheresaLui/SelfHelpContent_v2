<properties
	  pageTitle=".Net: Change Feed: System.ArgumentException"
	  description=".Net: Change Feed: System.ArgumentException"
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
	  articleId="ffade283-66ee-47fa-a462-d2dadd478434"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# .Net: Change Feed: System.ArgumentException

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

#### Issue: System.ArgumentException (Lease Collection Not Found)

if you get an error like

`
System.ArgumentException: The lease collection, if partitioned, must have partition key equal to id.
`

This can happen because they are using an invalid configured lease collection, so check that first.

If that looks configured right (pk = "/id"), then it's likely a typo. If they mistype the collection or database name, it will result in a 404 which will generate that error from ChangeFeedProcessor. Get them to double check all their names and match them to the names you see in ReportQuota5M table for that GBDA for that time period.

```
ReportQuota5M
| where TIMESTAMP > ago(1d)
| where GlobalDatabaseAccountName == "xxxxxxxxxxxx"
| distinct CollectionName, CollectionRid, DatabaseName, DatabaseRid
```

It is a good idea to ask for a ReadOnly key and try to repro yourself if the customer still thinks there is an issue after double checking these things.


If you can't debug it, assign to Change Feed queue and provide:

- Error message
- Repro code
- Global Database Account Name
- Database Name
- Collection Name
- Lease Database Name
- Lease Collection Name
- (always) Read only key for repro purposes
- Timestamps of last error seen


## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query, you can share the output table but make sure to not incude any internal information.

<!--/issueDescription-->

