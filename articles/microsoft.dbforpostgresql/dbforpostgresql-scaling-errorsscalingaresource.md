<properties
    pageTitle="Error while scaling a resource in Azure Database for PostgreSQL"
    description="Error while scaling a resource in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32639978, 32780930"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7a89af74-874f-4cc1-a34b-77fdb5a0be0d"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Error while scaling a resource in Azure Database for PostgreSQL

Most users are able to resolve their issues using the steps below.

## **Recommended Steps**

* Are you trying to switch from Basic to General Purpose/Memory Optimized service tiers or vice-versa?

    * If you want to switch from Basic to General Purpose or Memory Optimized, or vice-versa, follow the steps in the [Upgrade from Basic to General Purpose or Memory Optimized tiers in Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/690976) blog.

* Are you experiencing dropped connections and finding that you can't establish new connections while compute (vCores) scaling operation is in progress?

    * vCore scaling requires a server restart. The window when new connections can't be established varies, but in most cases, the window is less than a minute. We recommend that you implement retry logic so that your application can seamlessly reconnect to the Postgres server after the scale operation is completed. Storage scaling doesn't cause a restart.

* Would you like to scale up the primary server with a replica, but it doesn't work? Are you trying to scale down a replica?

    * Before you update a primary server configuration to new values, update the replica configuration to equal or greater values.

* Are you getting this error: "Service is temporarily busy and the operation cannot be performed. Please try again later"?

    * Try to scale the server again, after a few minutes.

* Are you attempting to scale storage beyond 4 TB and can't do it?
 
    * Your server may be running on a legacy storage option supporting up to 4 TB only. To upgrade your server to support up to 16 TB, perform a dump and restore to a new server created with the storage size that you want, including sizes between 4 TB and 16 TB.

* Are you trying to use the Azure Monitor auto-scale feature with Azure Database for PostgreSQL - Single server? 
* 
    * Azure Monitor auto-scale feature is not supported for Azure Database for PostgreSQL - Single server. However, you can configure auto-scaling using Azure run books. See [How to auto-scale an Azure Database for PostgreSQL/MySQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**

* [Azure Postgres compute and storage tiers](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)<br>
* [Read Replica in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#replica-configuration/)<br>
* [Azure Database for PostgreSQL Pricing Page](https://azure.microsoft.com/pricing/details/postgresql/)
