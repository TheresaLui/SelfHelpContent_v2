<properties
	pageTitle="Jupyter Notebooks"
	description="Enable Jupyter Notebooks"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32688847"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-notebooks"
	displayOrder="91"
	category="Azure Cosmos DB - Notebooks"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Jupyter Notebooks

**Problem**

Unable to create account with notebooks, or enable notebooks on an existing account.

## **Recommended Steps**

Built-in notebooks for Azure Cosmos DB are currently available in [29 Azure regions](https://docs.microsoft.com/azure/cosmos-db/enable-notebooks#supported-regions). To use notebooks, create a new account or enable notebooks on an existing account in one of the supported regions. 

Starting February 10, 2021, new Cosmos accounts created in supported regions will automatically have notebooks enabled. There is no configuration required during account creation. After creating the account, you can access your notebooks workspace in Data Explorer. 

### **500 Errors While Loading Notebooks**  
If you are receiving 500 errors while loading your notebooks, typically this is caused by exceeding memory in your workspace. Resetting your workspace should correct the problem. 
- Please click on *Reset Workspace* option on data explorer page and allow some time for the operation to complete. Once completed you should be able to recover your notebooks.


### **Recommended Documents**  

[Enable built-in notebooks](https://docs.microsoft.com/azure/cosmos-db/enable-notebooks)
<br>This article describes how to enable this feature for your Azure Cosmos DB account.  

[How to use C# notebook features](https://docs.microsoft.com/azure/cosmos-db/use-csharp-notebook-features-and-commands)
<br>This article describes how to use built-in C# notebook commands and features to do common operations.

[How to use Python notebook features](https://docs.microsoft.com/azure/cosmos-db/use-python-notebook-features-and-commands)
<br>This article describes how to use built-in Python notebook commands and features to do common operations.

