<properties
	  pageTitle="Understand error User does not have access to perform the specified operation"
	  description="Understand error User does not have access to perform the specified operation"
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
	  articleId="dd145cb0-5bc1-4646-82a0-6e021707eebc"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Understand error User does not have access to perform the specified operation

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Investigation (not customer message):**
Unable to access the Cosmos DB in Portal or Cosmos DB Portal Overview page fails with Access Denied. User is the owner of the Cosmos DB Account or does have full control permission. But still the below exception is shown in the portal.


**Symptom**:
![Error message image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EQR41VCB2ANGpJD9VwybmfMBOg4fTqxXQzdX8TyKLKbWPg?e=J2SanN)

**Exception**

`
Microsoft_Azure_DocumentDB]  11:32:34 AM DocumentDBClientProxy DocumentDBClientProxy: {"textStatus":"error","errorThrown":"","url":"https://main.documentdb.ext.azure.com/api/RuntimeProxy?resourceUrl=https%3A%2F%2Fion-platform-db-qa.documents.azure.com%3A443%2Fdbs&rid=&rtype=dbs&sid=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx&rg=BUY.NDX.ION.PLATFORM-QA&dba=ion-platform-db-qa","method":"GET","responseHeaders":"pragma: no-cache\r\ncontent-type: application/json; charset=utf-8\r\ncache-control: no-cache\r\nexpires: -1\r\n","xhr":{"readyState":4,"responseText":"{\"message\":\"User does not have access to perform the specified operation\\r\\nActivityId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, documentdb-dotnet-sdk/1.20.0 Host/64-bit MicrosoftWindowsNT/10.0.14393.0\"}","status":500,"statusText":"error"}}
`
 
`
[Microsoft_Azure_DocumentDB]  11:32:34 AM CollectionDataUtilities CollectionDataUtilities: {"code":500,"body":"{\"message\":\"User does not have access to perform the specified operation\\r\\nActivityId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, documentdb-dotnet-sdk/1.20.0 Host/64-bit MicrosoftWindowsNT/10.0.14393.0\"}"}
`

<br>

#### Back ground/Cause
 
ARM have released a feature called ?Blue Print? which basically helps to ACL a deny permission.   This feature is basically restricting the portal to get the Cosmos DB key triggering the below issue.

You can confirm that the ARM is causing the issue by Query in ARM Prod Kuto endpoint.  Any result from the query does indicate that the Blue Print/ARM is causing this issue.

```
Traces
| where TIMESTAMP > ago(1d)
| where operationName == "AuthorizationFilterEngine.FilterResourcesByDenyAssignment"
| where message startswith "Received '0' resources. Returning '0' resources after filtering by deny assignment. Orignial groups count"
| where subscriptionId =="xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
| project TIMESTAMP, ActivityId, subscriptionId, operationName,message
| limit 10
```
<br>

	
|TIMESTAMP|ActivityId|subscriptionId|operationName|message|
|-|-|-|-|-|
|2019-06-12 13:42:11.5788270|xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx|xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx|AuthorizationFilterEngine.FilterResourcesByDenyAssignment|Received '0' resources. Ret|

<br>
<br>

###Quick way to Confirm ARM issue
 

You can run the Azure CLI and if the keys are not shown then the arm is not returning the keys due to the ACL from Blue Print.
`
az cosmosdb list-read-only-keys --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup
`

###Example  
`
az cosmosdb list-read-only-keys --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup
`

<br>
 
#### Mitigation
- They can use the sunset link if they have connection string for cosmosdb account.  
or
- They need to remove the Deny by removing configuration through Blue Print.

<br>

#### Engineering Engagement 
 
Please raise a CRI to Azure ARM Team.  You can also check the status from the CRI https://portal.microsofticm.com/imp/v3/incidents/details/123438318/home


## Customer message:

Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query, you can share the output table but make sure to not incude any internal information.

<!--/issueDescription-->

