<properties
    pageTitle="Error while scaling a resource in Azure Database for PostgreSQL"
    description="Error while scaling a resource in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32790088"
    resourceTags="servers, databases"
    productPesIds="17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ad7c4493-8675-4ab0-9466-4ae8ff066ca4"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Scaling compute within a tier in Azure Database for PostgreSQL

You can scale compute (i.e vCores) up/down to accommodate the changing workload requirements. For example, during off-peak hours, you may want to scale-down the compute or scale-up as the demand increases. The following are some of the common questions related to scaling vCores.

## **Recommended Steps**

* Are you experiencing dropped connections or you're finding that you can't establish new connections while compute (vCores) scaling operation is in progress?

    Compute scaling requires a server restart. The window when new connections can't be established varies as it de[ends on the recovery time but if you scale compute during low transactional activity time, it should take a minute or two. We recommend that you implement retry logic so your application can seamlessly reconnect to the PostgreSQL server, after the scale operation is completed.

* Would you like to scale up compute on the primary server with a replica and it doesn't work? Are you trying to scale down a replica?

    Azure PostgreSQL runs community PostgreSQL engine and it requires that replica server must have set [max_connections](https://www.postgresql.org/docs/current/runtime-config-connection.html) >= primary server. In Single Server, the max_connections is tightly coupled with vCores. For this reason, you must scale the compute on replica first before scaling the primary.

* Are you getting this error: "Service is temporarily busy and the operation cannot be performed. Please try again later"?

    Try to scale the server again, after a few minutes.

* Are you trying to use the Azure Monitor auto-scale feature with Azure Database for PostgreSQL - Single server? 

    Azure Monitor auto-scale feature is not supported for Azure Database for PostgreSQL - Single server. However, you can configure auto-scaling using Azure run books. See [How to auto-scale an Azure Database for PostgreSQL/MySQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**
* [Azure Postgres compute and storage tiers](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)<br>
* [Read Replica in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#replica-configuration/)<br>
* [Azure Database for PostgreSQL Pricing Page](https://azure.microsoft.com/pricing/details/postgresql/)