<properties
	selfHelpType = "generic"
	cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738808"
	displayOrder = ""
	diagnosticScenario = ""
	pageTitle = "Authentication failure/SQL on-demand Azure Active Directory Authentication"
	description = "Authentication failure/SQL on-demand Azure Active Directory Authentication"
	infoBubbleText = ""
	articleId = "synapse-authenticationfailure-sqlondemandazureactivedirectoryauthentication"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>

# Authentication failure/SQL on-demand Azure Active Directory Authentication

## **Recommended Steps**

* Check if you have permissions to log into SQL on-demand. To gain access, one of the Azure Synapse workspace administrators should add you to workspace administrator or SQL administrator role. [Visit full guide on access control for more information](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/access-control?branch=release-ignite-arcadia).

* Make sure you are connecting to database you are given access to. To connect to specific database using SSMS, check [Connect to Server (Connection Properties Page)](https://docs.microsoft.com/sql/ssms/f1-help/connect-to-server-connection-properties-page-database-engine?view=sql-server-ver15). For ADS, check [Use Azure Data Studio to connect and query](https://docs.microsoft.com/sql/azure-data-studio/quickstart-sql-database?view=sql-server-ver15).

* If using Synapse Studio, your network might prevent communication to Azure Synapse backend. Most frequent case is that port 1443 is blocked. To get the SQL on-demand to work unblock this port. Other problems could prevent SQL on-demand to work as well, [visit full troubleshooting guide for more information](https://review.docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio?branch=release-ignite-arcadia).

* If using SSMS or ADS, check if your network blocks port 1433.

* If using ADF to access SQL on-demand, check if MSI account for your workspace is given permission to log in. [Visit full guide on access control for more information](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/access-control?branch=release-ignite-arcadia)


