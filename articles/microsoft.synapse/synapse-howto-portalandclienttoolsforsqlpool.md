<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738790"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "How-To/Portal and Client Tools for SQL pool"
	description = "How-To/Portal and Client Tools for SQL pool"
	articleId = "synapse-howto-portalandclienttoolsforsqlpool"
	authors = "saltug"
	ms.author = "saltug"
/>

# How-To/Portal and Client Tools for SQL pool

## **Recommended Steps**

* To ensure latest feature support, we recommend using the [latest version of SQL Server Database tools (SSDT) and Visual Studio for development purposes](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-install-visual-studio)
* Monitoring resource utilization and query activity [from Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-concept-resource-utilization-query-activity)

  * When viewing resource utilization from the Azure portal, the metric aggregation occurs across all the compute nodes of the data warehouse. For data warehouses with a single compute node (DW500c and below), Max, Min, and Avg will have the same values.

* [Azure Data Studio quickstart to connect and query Azure SQL Database](https://docs.microsoft.com/sql/azure-data-studio/quickstart-sql-database?toc=%2Fazure%2Fsql-database%2Ftoc.json&view=sql-server-2017?WT.mc_id=pid:13491:sid:32630411/)

## **Recommended Documents**

* [Query with SSMS](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-query-ssms)
* [Query with Visual Studio](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-query-visual-studio)
* [Manageability and monitoring](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-overview-manageability-monitoring)
* [Understanding metrics and logs available in the Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-concept-resource-utilization-query-activity)


