<properties
	pageTitle="My database is slow"
	description="My database is slow"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="databases, servers"
	productPesIds=""
	cloudEnvironments="public"
/>

# My database is slow

## **Recommended steps**
Missing indexes and poorly optimized queries are common reasons for poor database performance. First identify opportunities to fine tune these by using "Query Performance Insight" and "Index advisor tools" using the links below. If the problems persist, consider changing the service tier of a single database or increasing the eDTUs of an elastic database pool at any time to improve performance.

* Use [Query Performance Insight](data-blade:SqlAzureExtension.QueryPerformanceBlade) to find the top consuming queries and identify the ones that have to be fixed.
* Use [SQL Database Advisor](data-blade:SqlAzureExtension.DatabaseRecommendationBlade) to get index recommendations and create indexes.
* Analyze the metrics shown on the SQL server resource blade to identify whether any resource is being overutilized or throttled. Mitigate resource issues by scaling up or out.<br>
[Understand what's available in each service tier](https://azure.microsoft.com/documentation/articles/sql-database-service-tiers/)
* For multiple databases,  scale resources automatically with Elastic Database Pool.<br>
[Understand elastic database pools](https://azure.microsoft.com/documentation/articles/sql-database-elastic-pool-guidance/)

## **Recommended documents**
[Troubleshoot Azure SQL Database performance](https://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-performance/)<br>
[Monitoring using DMVs](https://azure.microsoft.com/documentation/articles/sql-database-monitoring-with-dmvs/)<br>
[Extended Events](https://azure.microsoft.com/documentation/articles/sql-database-xevent-db-diff-from-svr/)<br>
[Benchmark overview](https://azure.microsoft.com/documentation/articles/sql-database-benchmark-overview/)
