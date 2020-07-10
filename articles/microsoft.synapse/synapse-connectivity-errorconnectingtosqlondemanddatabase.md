<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738769"
	displayOrder = ""
	diagnosticScenario = ""
	pageTitle = "Connectivity/Error connecting to SQL on-demand database"
	description = "Connectivity/Error connecting to SQL on-demand database"
	infoBubbleText = ""
	articleId = "synapse-connectivity-errorconnectingtosqlondemanddatabase"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>

# Connectivity/Error connecting to SQL on-demand database

## **Recommended Steps**

* Check if you have permissions to log into SQL on-demand. To gain access, one of the Azure Synapse workspace administrators should add you to workspace administrator or SQL administrator role. [Visit full guide on access control for more information](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control). 

* Make sure you are connecting to database you are given access to. To connect to specific database using SSMS, check [Connect to Server (Connection Properties Page)](https://docs.microsoft.com/sql/ssms/f1-help/connect-to-server-connection-properties-page-database-engine?view=sql-server-ver15). For ADS, check [Use Azure Data Studio to connect and query](https://docs.microsoft.com/sql/azure-data-studio/quickstart-sql-database?view=sql-server-ver15). 

* To gain access, one of the Azure Synapse workspace administrators should add you to workspace administrator or SQL administrator role. [Visit full guide on access control for more information](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control). 

* If using Synapse Studio, check if your network blocks port 1443 and unblock it. 

* If using SSMS or ADS, check if your network blocks port 1433 and unblock it. 


