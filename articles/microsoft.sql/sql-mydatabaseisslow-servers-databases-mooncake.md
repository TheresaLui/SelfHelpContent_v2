<properties
	pageTitle="My database is slow"
	description="My database is slow"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="12"
	selfHelpType="resource"
	supportTopicIds="31980430, 31980438"
	resourceTags="databases, servers"
	productPesIds="13491"
	cloudEnvironments="MoonCake"
/>

# My database is slow

## **Recommended steps**
Missing indexes and poorly optimized queries are common reasons for poor database performance. First identify opportunities to fine tune these by using "Query Performance Insight" and "Index advisor tools" using the links below. If the problems persist, consider changing the service tier of a single database or increasing the eDTUs of an elastic database pool at any time to improve performance.

* Use [Query Performance Insight](data-blade:SqlAzureExtension.QueryPerformanceBlade) to find the top consuming queries and identify the ones that have to be fixed.
* Use [SQL Database Advisor](data-blade:SqlAzureExtension.DatabaseRecommendationBlade) to get index recommendations and create indexes.
* Analyze the metrics shown on the SQL server resource blade to identify whether any resource is being overutilized or throttled. Mitigate resource issues by scaling up or out.<br>
[Understand what's available in each service tier](https://docs.azure.cn/sql-database/sql-database-service-tiers/)
* For multiple databases,  scale resources automatically with Elastic Database Pool.<br>
[Understand elastic database pools](https://docs.azure.cn/sql-database/sql-database-elastic-pool-guidance/)

## **Recommended documents**
[Troubleshoot Azure SQL Database performance](https://docs.azure.cn/sql-database/sql-database-troubleshoot-performance/)<br>
[Monitoring using DMVs](https://docs.azure.cn/sql-database/sql-database-monitoring-with-dmvs/)<br>
[Extended Events](https://docs.azure.cn/sql-database/sql-database-xevent-db-diff-from-svr/)<br>
[Benchmark overview](https://docs.azure.cn/sql-database/sql-database-benchmark-overview/)
