<properties
    pageTitle="Error while scaling a resource in Azure Database for PostgreSQL"
    description="Error while scaling a resource in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="00000000"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="49dc3f02-f525-4922-a6fe-f9e4b7d1c92c"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Scaling across compute tiers in Azure Database for PostgreSQL

Each compute tier offers a unique proposition and usage scenario. For example, Basic tier is low cost and targets developers and the workloads with low transactional activity and throughput. General Purpose and Memory optimized tiers target enterprise workloads that require higher predictable performance. Customers can choose to move between these compute tiers as the demands on the workload changes.

## **Recommended Steps**

* Are you trying to scale from Basic tier to General Purpose/Memory Optimized service tiers or vice-versa?

    Scaling out of or into Basic requires a transition into a different storage architecture and therefore requires a database copy. Please follow the steps in the [Upgrade from Basic to General Purpose or Memory Optimized tiers in Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/690976) blog.

* Are you scaling out of General Purpose to Memory Optimized tiers or vice-versa?

    Scaling to different database tier is done by creating a new container for the database service. Once the new container is available, the database service fails over. All existing connections are closed. There is no change to the connection strings but the application must re-establish the connection. If your application connects using a connection pooler, it can re-establish the connections.

* Are you trying to use the Azure Monitor auto-scale feature with Azure Database for PostgreSQL - Single server? 
 
    Azure Monitor auto-scale feature is not supported for Azure Database for PostgreSQL - Single server. However, you can configure auto-scaling using Azure run books. See [How to auto-scale an Azure Database for PostgreSQL/MySQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**

* [Azure Postgres compute and storage tiers](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)<br>
* [Read Replica in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#replica-configuration/)<br>
* [Azure Database for PostgreSQL Pricing Page](https://azure.microsoft.com/pricing/details/postgresql/)
