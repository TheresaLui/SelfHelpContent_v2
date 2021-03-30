<properties
	  pageTitle="Restrict Application using Master Key for non-CRUD operation issue"
	  description="Restrict Application using Master Key for non-CRUD operation issue"
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
	  articleId="23a820ed-1001-4d6d-973a-b890a967ec01"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Restrict Application using Master Key for non-CRUD operation issue

<!--issueDescription-->

Dear customer,

To restrict Application using Master Key for non-CRUD operation or Only to do CRUD operations, in Cosmos DB operation can be any of the operation type listed below.

| OperationType       | Operations                                                   | Azure Active Directory Identity | Keys and resource tokens |
| ------------------- | ------------------------------------------------------------ | :-----------------------------: | :----------------------: |
| Account Management  | Control global replication<br />Setup virtual network integration, firewall and CORS<br /> Regenerate master Kyes<br />Access to monitoring and Metrics<br />Set Account consistently |               Yes               |            No            |
| Resource Management | Create Database and containers<br />Update Index Policies<br />Set container's throughput (RUs) |               Yes               |           Yes            |
| Data Operations     | CRUD Operations<br />Run Queries<br />Manage and run stored procedures, UDF and triggers |               Yes               |           Yes            |

The Resource Management  operation can be performed through any of the below method.
1. Azure Portal (The portal     still uses the Master key but this would be changed in near future)
2. Arm calls      (Template /Scripting through ARM call) 
3. Applications with connection string.

The delete from Arm Calls **are linked to a user identity.**  However, the other methods **uses the Master Key to access the Cosmos DB and does not have any user identity associated with**.  So, no identity is mapped if the delete/create/update  is performed using master key.

We do have procedure documented to [restrict access](https://docs.microsoft.com/en-us/azure/cosmos-db/how-to-restrict-user-data) the resource management actions through master key. 

Once you restrict the [access](https://docs.microsoft.com/en-us/azure/cosmos-db/how-to-restrict-user-data#disallow-the-execution-of-non-data-operations), the applications using the master key would fail with the below error message if its tries to drop the resource.  The delete or create operation are only allowed  through the ARM provider. 

**`"*Operation 'DELETE' on resource 'dbs' is not allowed through Azure Cosmos DB endpoint. Please switch on such operations for your account, or perform this operation through Azure Resource Manager, Azure Portal, Azure CLI or Azure Powershell"*`**

**`*ActivityId: 30f0d891-1269-4f06-9165-66cfa788ccca, Microsoft.Azure.Documents.Common/2.9.2, documentdb-dotnet-sdk/2.8.1 Host/64-bit MicrosoftWindowsNT/6.2.9200.0*`**

You can use the Azure Activity log / Azure Diagnostic logging  to track all the resource management operation.

Thank you.

<!--/issueDescription-->

