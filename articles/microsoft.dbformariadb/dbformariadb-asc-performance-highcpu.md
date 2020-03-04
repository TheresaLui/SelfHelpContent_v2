<properties
    pageTitle="Orcas MariaDB server is facing high CPU usage"
    description="Orcas MariaDB server is facing high CPU usage"
    infoBubbleText="Server is facing high CPU usage. See details on the right"
    service="microsoft.dbformariadb"
    resource="dbformariadb"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformariadb-asc-performance-highcpu"
    diagnosticScenario="OrcasMariaDBHighCPU"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Server is facing high CPU usage

<!--issueDescription-->
Thank you for contacting Microsoft support about your performance issues with your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that your CPU percent is above 90% for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. High CPU percent could be due to multiple causes.
<!--/issueDescription-->

## **Recommended Steps**

* Review *CPU percent* in the Metrics window of the portal. If CPU spikes correlate with times when you increased your query workload, consider scaling up vCores to increase compute.
* Compare *Active Connections* and *CPU percent* side-by-side in the Metrics window. If your increases in active connections correlate with CPU spikes, consider using a connection pooler between your application and MariaDB server. Connection pooler would help optimize connection management.
* Use the Intelligent Performance features for additional insights. For more information, visit the [Performance Recommendations document](https://docs.microsoft.com/azure/mariadb/concepts-performance-recommendations)

## **Recommended Documents**

* [Performance Recommendations in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-performance-recommendations)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)
* [Query Performance Insight in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-query-performance-insight)
* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)