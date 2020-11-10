<properties
    pageTitle="Orcas MySQL server is facing high CPU usage"
    description="Orcas MySQL server is facing high CPU usage"
    infoBubbleText="Server is facing high CPU usage. See details on the right"
    service="microsoft.dbformysql"
    resource="dbformysql"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformysql-asc-performance-highcpu"
    diagnosticScenario="OrcasMySQLHighCPU"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Server is facing high CPU usage

<!--issueDescription-->
During our investigation regarding performance issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName--> we found that your CPU percent is above 90% for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). High CPU percent could be due to multiple causes.
<!--/issueDescription-->

## **Recommended Steps**

* Review *CPU percent* in the Metrics window of the portal. If CPU spikes correlate with times when you increased your query workload, consider scaling up vCores to increase compute.
* Compare *Active Connections* and *CPU percent* side-by-side in the Metrics window. If your increases in active connections correlate with CPU spikes, consider using a connection pooler between your application and MySQL server. Connection pooler would help optimize connection management.
* Use the Intelligent Performance features (only in MySQL 5.7, 8.0) for additional insights. For more information, visit the [Performance Recommendations document](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations).

## **Recommended Documents**

* [Performance Recommendations in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
* [Query Performance Insight in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
