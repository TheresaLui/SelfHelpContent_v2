<properties
	pageTitle="Specific errors or exceptions"
	description="Specific errors or exceptions"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,mlee3gsd"
	ms.author="saltug,martinle"
	supportTopicIds=""
	productPesIds=""
	displayOrder="9"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-performanceandqueryexecution-specificerrorsorexceptions-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>

# Specific errors or exceptions

## **Recommended Steps**

* To resolve out of memory errors, [try increasing the user's resource class](https://docs.azure.cn/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class) or [scale your data warehouse to a larger service level](https://docs.azure.cn/sql-data-warehouse/quickstart-scale-compute-portal)
* To resolve syntax error for queries, check the [T-SQL syntax](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-reference-tsql-statements)
* To resolve error `Database 'Distribution_40_Cache' cannot be opened due to inaccessible files or insufficient memory or disk space`, try pausing and resuming your data warehouse

## **Recommended Documents**

* [Additional Troubleshooting](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-troubleshoot)
