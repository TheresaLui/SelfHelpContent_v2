<properties
	pageTitle="100% CPU usage"
	description="100% CPU usage"
	infoBubbleText="Found recent issue. See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-merupg-performance-hundredpercentcpu"
	diagnosticScenario="OrcasMeruPGHundredPercentCPUInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32639959, 32639953"
	resourceTags=""
	productPesIds="17069"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# 100% CPU utilization

<!--issueDescription-->
CPU usage was 100% <!--$Count-->Count<!--/$Count--> times on Postgres server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC).
<!--/issueDescription-->


## **Recommended Steps**

* CPU usage can spike for short periods to run a query or execute a backend task. It should normally return to lower usage quickly. 

* If CPU is currently at 100%, this may indicate a stuck long-running process. Run the query `SELECT pid, now() - pg_stat_activity.query_start AS duration, query, state FROM pg_stat_activity ORDER BY duration LIMIT 5;` to identify the longest-running processes. 

* If there was a sudden increase in number of connections that corresponds with the CPU growth, it indicates the Postgres CPU was busy with connection handling. Avoid frequently opening short connections, since that is likely to increase CPU usage. We recommend using [a connection pooler like pgBouncer](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/steps-to-install-and-setup-pgbouncer-connection-pooling-proxy/ba-p/730555) to help manage connections.

* Consider scaling up to a higher compute tier if the workload has increased
