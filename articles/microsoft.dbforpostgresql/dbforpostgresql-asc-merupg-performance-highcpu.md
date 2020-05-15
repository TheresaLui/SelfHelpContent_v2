<properties
	pageTitle="High CPU usage"
	description="High CPU usage"
	infoBubbleText="Found recent connection failure. See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-merupg-performance-highcpu"
	diagnosticScenario="OrcasMeruPGPerfHighCPUInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32639959"
	resourceTags=""
	productPesIds="17069"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# High CPU usage

<!--issueDescription-->
CPU has been above <!--$PerfThreshold-->PerfThreshold<!--/$PerfThreshold--> for <!--$PerfTimeThreshold-->PerfTimeThreshold<!--/$PerfTimeThreshold--> on Postgres server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC).
<!--/issueDescription-->


## Recommended steps

* If there was a sudden increase in number of connections that corresponds with the CPU growth, it indicates the Postgres CPU was busy with connection handling. Avoid frequently opening short connections, since that is likely to increase CPU usage. We recommend using [a connection pooler like pgBouncer](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/steps-to-install-and-setup-pgbouncer-connection-pooling-proxy/ba-p/730555) to help manage connections.


* What query was running when CPU went high? If CPU is currently high, run `SELECT * FROM pg_stat_activity;` to look at the currently running queries and processes. 

* Consider scaling up to a higher compute tier if the workload has increased.