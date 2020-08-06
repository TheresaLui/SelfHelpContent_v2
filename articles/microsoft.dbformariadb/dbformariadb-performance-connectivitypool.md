<properties
    pageTitle="High percentage of short-lived connections"
    description="High percentage of short-lived connections"
    infoBubbleText="Customer has high percentage of short-lived connections. See details on the right"
    service="microsoft.dbformariadb"
    resource="dbformariadb"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformariadb-performance-connectivitypool"
    diagnosticScenario="OrcasMariaDBConnectionPool"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# High percentage of short-lived connections

<!--issueDescription-->
During our investigation regarding performance issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we found that 80% of connections are being closed under 1 second between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). Opening new connections is an expensive operation. The high frequency of connection open/close is likely consuming server resources and making queries slower.
<!--/issueDescription-->

## **Recommended Steps**

Consider using a connection pool between your application and MariaDB server to optimize connection management. A connection pooler will reuse connections instead of opening new ones.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)