<properties
	  pageTitle="Create or Delete Collection/Dabase issue Investigation"
	  description="Create or Delete Collection/Dabase issue Investigation"
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
	  articleId="7162b465-6216-47ed-a860-e2dc525ffd09"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Create or Delete Collection/Dabase issue Investigation

#Collection Create

If the customer would like to know When and Who (user agent) created a collection, you could use the following query replacing <CustomerDatabaseAccountName> with the name of the global database account for the customer you are working with.

```
Request5M
| where globalDatabaseAccountName == "CustomerDatabaseAccountName"
| where verb =="POST" and category  contains "Collection"
| where isQuery == bool(0)
| summarize  min(TIMESTAMP), max(TIMESTAMP) by category, isQuery, userAgent

#Database or Collection Delete

The rest API call for the collection/Database delete does provide you the verb which would be logged in the Request 5M. https://docs.microsoft.com/en-us/rest/api/cosmos-db/delete-a-collection

https://docs.microsoft.com/en-us/rest/api/cosmos-db/delete-a-database

 
In the collection case, the Verb is "DELETE".  

 
The userAgent column should have the information on how the Delete was performed.  The value "Azure portal" would mean it was performed through Azure portal.  Any other would be the respective API call.

 
[See Request5M Kusto Table](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/237557)

```
Request5M

| where globalDatabaseAccountName =="prodexos"  and TIMESTAMP  > ago(7d) and category =="Collection" and verb =="DELETE"
| project TIMESTAMP , globalDatabaseAccountName , category , verb , userAgent , collectionResourceId , databaseResourceId , hostname , region
```

#User Information
You can connect to Azure portal Endpoint to extract the user information If the delete was performed through Azure Portal.  Please engage the Azure Support Team if you do not have access to this endpoint.  Also, do not share the Userid information, instead request the customer to share all the user ID with PUID who have access to the account and we can point the user who delete the collection or database.

Endpoint : azportalpartner.kusto.windows.net
 
```
ExtTelemetry
| where extension == "Microsoft_Azure_DocumentDB"
| where source == "DataExplorer"
| where action contains "DeleteCollection"
| where ['data'] contains "prodexos"
| parsed_data = parse_json(['data'])
| where tostring(parsed_data.data.collectionId) != "" 
| summarize by tostring(parsed_data.data.collectionId), userId , tenantId, bin(TIMESTAMP, 2h) 

