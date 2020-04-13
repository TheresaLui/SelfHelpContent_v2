<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738767"
	displayOrder = ""
	diagnosticScenario = ""
	pageTitle = "SQL Performance and Query Execution/Data export using CETAS in SQL on-demand"
	description = "SQL Performance and Query Execution/Data export using CETAS in SQL on-demand"
	infoBubbleText = ""
	articleId = "synapse-sqlperformanceandqueryexecution-dataexportusingcetasinsqlondemand"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>

# SQL Performance and Query Execution/Data export using CETAS in SQL on-demand

## **Recommended Steps**

* Visit [CETAS](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/development-tables-cetas?branch=release-ignite-arcadia) for syntax and samples
* Make sure you are exporting data to supported storage account types as specified in [CETAS in SQL on-demand](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/development-tables-cetas?branch=release-ignite-arcadia)
* Make sure you created appropriate credential for both source and destination storage accounts as specified in [control storage access for SLQ on-demand](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/development-storage-files-storage-access-control?branch=release-ignite-arcadia), and have appropriate [permissions](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/development-tables-cetas?branch=release-ignite-arcadia#permissions) on destination storage account
* Make sure you use [data types supported by CETAS](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/development-tables-cetas?branch=release-ignite-arcadia#supported-data-types)
* Make sure destination storage account is in the same region your SQL on-demand endpoint is. You can find storage account and workspace regions on Azure Portal, in Overview blades of your storage account and workspace.
