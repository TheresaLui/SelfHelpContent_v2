<properties
    pageTitle="High percentage of short-lived connections"
    description="High percentage of short-lived connections"
    infoBubbleText="Customer has high percentage of short-lived connections. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="danielcarbajal"
    ms.author="dacarbaj"
    displayOrder="100"
    articleId="dbforpostgresql-asc-performance-connectivitypool"
    diagnosticScenario="OrcasPostgresConnectionPool"
    selfHelpType="rca"
    supportTopicIds="32639985,32639986,32639987,32640019,32640025,32640026,32640027"
    resourceTags="windows, linux"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# High percentage of short-lived connections

<!--issueDescription-->
Thank you for contacting Microsoft support about your performance issues with your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that 80% of connections are being closed under 1 second between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. Opening new connections is an expensive operation. The high frequency of connection open/close is likely consuming server resources and making queries slower.
<!--/issueDescription-->

## **Recommended Steps**

Consider using a connection pooler like pgBouncer between your application and Postgres server to optimize connection management. A connection pooler will reuse connections instead of opening new ones.

## **Recommended Documents**

* [Learn more about why we recommend pgBouncer](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Not-all-Postgres-connection-pooling-is-equal/ba-p/825717)<br>
* [Set up pgBouncer](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Steps-to-install-and-setup-PgBouncer-connection-pooling-proxy/ba-p/730555)<br>
* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)