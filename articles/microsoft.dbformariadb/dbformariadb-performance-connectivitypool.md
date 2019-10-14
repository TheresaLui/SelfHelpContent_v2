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
    diagnosticScenario="OrcasMariadbConnectionPool"
    selfHelpType="rca"
    resourceTags="servers, databases"
    cloudEnvironments="public"
/>

# High percentage of short-lived connections

<!--issueDescription-->
Thank you for contacting Microsoft support about your performance issues with your Mariadb server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that 80% of connections are being closed under 1 second between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. Opening new connections is an expensive operation. The high frequency of connection open/close is likely consuming server resources and making queries slower.
<!--/issueDescription-->

## **Recommended Steps**

Consider using a connection pool between your application and Mariadb server to optimize connection management. A connection pooler will reuse connections instead of opening new ones.

## **Recommended Documents**

* [Learn more about why we recommend connection pooling](https://docs.azure.cn/en-us/mysql-database-on-azure/mysql-database-connection-pool#-)<br>
* [Troubleshoot common connectivity issues to Azure Databases for Mariadb](https://docs.microsoft.com/en-us/azure/mariadb/howto-troubleshoot-common-connection-issues)