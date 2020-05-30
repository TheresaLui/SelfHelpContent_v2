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

Built-in notebooks for Azure Cosmos DB are currently available in the following Azure regions: Australia East, East US, East US 2, North Europe, South Central US, Southeast Asia, UK South, West Europe and West US 2.  
To use notebooks, create a new account with notebooks or enable notebooks on an existing account in one of these regions.  


### **500 Errors While Loading Notebooks**  
If you are receiving 500 errors while loading your notebooks, typically this is caused by exceeding memory in your workspace. Resetting your workspace should correct the problem. 
- Please click on *Reset Workspace* option on data explorer page and allow some time for the operation to complete. Once completed you should be able to recover your notebooks.


### **Recommended Documents**  

[Enable built-in notebooks](https://docs.microsoft.com/azure/cosmos-db/enable-notebooks)
<br>This article describes how to enable this feature for your Azure Cosmos DB account.  

[How to use notebook features](https://docs.microsoft.com/azure/cosmos-db/use-notebook-features-and-commands)
<br>This article describes how to use built-in notebook commands and features to do common operations.