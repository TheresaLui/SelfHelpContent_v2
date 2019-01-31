<properties
	pageTitle="query execution/performance and time outs"
	description="query execution/performance and time outs"
	service="microsoft.sql"
	resource="servers"
        authors="pxding"
        ms.author="pedin"
	displayOrder="6"
	selfHelpType="generic"
	supportTopicIds="31980430"
	resourceTags="databases, servers"
	productPesIds="13491"
	cloudEnvironments="public"
/>

# query execution/performance and time outs

## **Recommended steps**
Our internal service telemetry detected that there has been an increase in user requests for your database. This user load increase is potentially contributing to performance issues or timeouts due to lack of resources to execute the requested workload during that specific period. Please go through following documents:

## **Recommended documents**
* Poor performance in Azure SQL DB is most often either related to excessive CPU utilization or a query waiting on a resource.  
* The following reference walks through how to address both troubleshooting paths: 
* [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview)
* [Identify the queries which are causing the high CPU consumption](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance)
* [Enable Automatic tuning provides peak performance and stable workloads](https://docs.microsoft.com/azure/sql-database/sql-database-automatic-tuning)
* [Increase Azure Database tier to get more DTUs and hence accommodate for more workload](https://azure.microsoft.com/pricing/details/sql-database/single)
* [If the workload is varying, then consider moving few databases into SQL elastic pool to share DTUs](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)