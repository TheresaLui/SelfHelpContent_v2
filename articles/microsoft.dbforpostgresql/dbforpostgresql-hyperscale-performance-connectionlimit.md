<properties
    pageTitle="Connection limit on Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Connection limit on Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource=""
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-performance-connectionlimit.md"
    selfHelpType="generic"
    supportTopicIds="32640019"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Connection limit

Azure Database for PostgreSQL - Hyperscale (Citus) has a maximum connection limit of 300 connections on the coordinator node. For more information, please review the [limits documentation](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-configuration-options#limits-and-limitations).

## **Recommended Steps**
* We recommend that you set up and use [pgBouncer](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Steps-to-install-and-setup-PgBouncer-connection-pooling-proxy/ba-p/730555) or another connection pooler to manage connections. Server-side pgBouncer is not available in Azure Database for PostgreSQL - Hyperscale (Citus). 


