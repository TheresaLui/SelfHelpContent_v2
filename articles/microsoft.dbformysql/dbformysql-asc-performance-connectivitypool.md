<properties
    pageTitle="High percentage of short-lived connections"
    description="High percentage of short-lived connections"
    infoBubbleText="Customer has high percentage of short-lived connections. See details on the right"
    service="microsoft.dbformysql"
    resource="dbformysql"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformysql-asc-performance-connectivitypool"
    diagnosticScenario="OrcasMySQLConnectionPool"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# High percentage of short-lived connections

<!--issueDescription-->
During our investigation regarding performance issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName--> we found that 80% of connections are being closed under 1 second between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). Opening new connections is an expensive operation. The high frequency of connection open/close is likely consuming server resources and making queries slower.
<!--/issueDescription-->

## **Recommended Steps**

Consider using a connection pool between your application and MySQL server to optimize connection management. A [connection pooler](https://docs.microsoft.com/azure/mysql/concepts-connectivity#access-databases-by-using-connection-pooling-recommended) will reuse connections instead of opening new ones.

## **Recommended Documents**

* [Access databases by using connection pooling](https://docs.microsoft.com/azure/mysql/concepts-connectivity#access-databases-by-using-connection-pooling-recommended)
* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
