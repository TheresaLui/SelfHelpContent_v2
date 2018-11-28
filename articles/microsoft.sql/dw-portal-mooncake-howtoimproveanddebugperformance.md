<properties
	pageTitle="How to improve and debug performance"
	description="How to improve and debug performance"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="datawarehouse"
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# How to improve and debug performance

## **Recommended steps**
To resolve the most common performance issues, try the following methods.

1. Scaling SQL Data Warehouse up and down is easy and can provide a short burst of compute or a prolonged increase of performance.  If you are just starting out or have recently increased the amount of data you are working with we recommend trying a few DWU settings to understand which is right for you.<br>
[Learn more about scaling and DWUs](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-manage-compute-overview/)
2. Scaling your SQL Data Warehouse can impact concurrency.  Learn how you can manage concurrency with resource classes.<br>
[Resource Classes](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-develop-concurrency/)
3. Review our best practices for SQL Data Warehouse which gives several tips on getting your instance running smoothly and quickly.<br>
[SQL Data Warehouse Best Practices](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-best-practices/)

## **Recommended documents**
[Investigate Queries with DMVs](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-manage-monitor/)<br>
[Additional Troubleshooting](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-troubleshoot/)
