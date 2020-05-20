<properties
    pageTitle="Scaling Azure Database for PostgreSQL servers"
    description="Scaling Azure Database for PostgreSQL servers"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="190"
    selfHelpType="generic"
    supportTopicIds="32640014"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="09be710f-a2b7-4d3c-a6be-a6f466140475"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Scaling Azure Database for PostgreSQL servers

In Azure Database for PostgreSQL, scaling can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * If you want to switch from Basic to General purpose/Memory Optimized and vice-versa, please follow the steps in [Upgrade from Basic to General Purpose or Memory Optimized tiers in Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/690976) blog
    * If you want to migrate manually from Basic to General purpose/Memory Optimized and vice-versa, you can [take a database dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore) of your Basic tier PostgreSQL database, create a server in General Purpose/Memory Optimized and then load the database dump and vice-versa

* Connections are dropped and no new connections can be established while vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the Postgres server once the scale operation is completed. Storage scaling does not cause a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

    * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

* The Azure Monitor auto-scale feature is not supported in Azure Database for PostgreSQL. However, you can configure auto-scaling using Azure runbook and python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177)

## **Recommended Documents**

* [Azure Database for PostgreSQL Pricing Page](https://azure.microsoft.com/pricing/details/postgresql/)<br>
* [Migrate to Azure Database for PostgreSQL using dump and restore](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore/)<br>
* [Scaling resources in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#scale-resources/)<br>
* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
