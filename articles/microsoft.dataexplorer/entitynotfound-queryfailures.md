<properties
	pageTitle="Performance|Entity query failures" <!-- metadata only  -->
	description="Performance|Entity query failures" <!-- metadata only -->
    infoBubbleText="" <!-- notification presented in the Problem blade when an issue is found -->
	service="Microsoft.Kusto" <!-- name of the resource provider in ARM -->
	resource="clusters" <!-- ARM Name of the resource type -->
	authors="kustosee"
    ms.author="prvavill"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32613464,32613482,32613506"
	resourceTags=""
	productPesIds="16602"
	cloudEnvironments="Public"
    articleId="67CED318-3125-4546-BA44-FB23E224CC15"
	ownershipId="AzureDataExplorer_Kusto"
/>

# Azure Data Explorer query failures

## **Recommended Documents**

### Error E_ENTITY_NOT_FOUND: The requested entity was not found

- Your Azure Data Explorer is having entity was not found failures and this happens if database or table referenced in query does not exist in the Azure Data Explorer cluster. Use [this reference](https://docs.microsoft.com/azure/data-explorer/create-cluster-database-portal) to create database and [this reference](https://docs.microsoft.com/azure/data-explorer/kusto/management/tables) to create table to avoid this error.

