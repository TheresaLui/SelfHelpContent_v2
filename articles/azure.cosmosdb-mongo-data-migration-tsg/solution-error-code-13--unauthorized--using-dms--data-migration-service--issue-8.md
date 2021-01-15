<properties
	  pageTitle="Error code 13 (Unauthorized) using DMS (Data Migration Service) issue"
	  description="Error code 13 (Unauthorized) using DMS (Data Migration Service) issue"
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
	  articleId="8c873f3a-e734-4bba-881a-4293130d5d4f"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Error code 13 (Unauthorized) using DMS (Data Migration Service) issue

<!--issueDescription-->

Dear customer,

If you are getting the error ""_The connection failed. Engage: Mongo error code 13 (Unauthorized): Command listCollections failed: not authorized on Engage to execute command { listCollections: 1, $db: "Engage" }_"". 

DMS (Data Migration Service) needs only read permissions on the Native Mongo Source, following are operations used by DMS by database:

**admin**:  
buildInfo  
isMaster

**config**:  
databases  

**Collection being migrated:**  
Query  
Oplog Read

**db Level operations:**    
listIndexes    
collStats 

**In above following are the Diagnostic commands:**  
buildInfo  
collStats
 
For strict permission on the native source mongo db you need to create a customer role with the above permissions:
- https://docs.mongodb.com/manual/tutorial/manage-users-and-roles/#create-user-defined-role

<!--/issueDescription-->

