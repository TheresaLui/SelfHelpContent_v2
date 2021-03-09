<properties
    pageTitle="Scaling Azure Database for PostgreSQL servers"
    description="Scaling Azure Database for PostgreSQL servers"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="190"
    selfHelpType="generic"
    supportTopicIds="32640014, 32780933"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="09be710f-a2b7-4d3c-a6be-a6f466140475"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Scaling Azure Database for PostgreSQL servers

Most users are able to resolve their issues by using the steps below.

## **Recommended Steps**

* Are you trying to switch from Basic to General Purpose/Memory Optimized service tiers, or vice versa?

    * If you want to switch from Basic to General Purpose or Memory Optimized, or vice-versa, follow the steps in [Upgrade from Basic to General Purpose or Memory Optimized tiers in Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/690976) blog.

* Are you experiencing dropped connections and you're finding that you can't establish new connections while compute (vCores) scaling operation is in progress?

    * vCore scaling requires a server restart. The window when new connections can't be established varies, but in most cases, it is less than a minute. We recommend that you implement retry logic so your application can seamlessly reconnect to the Postgres server, after the scale operation is completed. Storage scaling does not cause a restart.

* Did you find out that your server is set to read only? Are you getting an error saying that your storage is almost full? 
* 
    * To avoid situation where Postgres becomes unresponsive, your server will be set to read-only when storage is almost full. When this occurs, you can either increase the size of provisioned storage, or start a new read-write session and drop some data to free storage. See [thresholds when server is set to read-only and steps to unlock writes](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#reaching-the-storage-limit).

* Would you like to scale up the primary server with a replica and it doesn't work? Are you trying to scale down a replica?

    * Before you update a master server configuration to new values, update the replica configuration to equal or greater values. This action ensures that the replica can keep up with any changes made to the master.

* Are you attempting to scale storage beyond 4 TB and can't do it?
 
    * Your server may be running on a legacy storage option supporting up to 4 TB only. To upgrade your server to support up to 16 TB, perform a dump and restore to a new server created with the storage size that you want, including sizes between 4 TB and 16 TB.

* Are you trying to use the Azure Monitor auto-scale feature with Azure Database for PostgreSQL - Single server? 
* 
    * Azure Monitor auto-scale feature is not supported for Azure Database for PostgreSQL - Single server. However, you can configure auto-scaling using Azure run books. See [How to auto-scale an Azure Database for PostgreSQL/MySQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**

* [Azure Database for PostgreSQL Pricing Page](https://azure.microsoft.com/pricing/details/postgresql/)<br>
* [Migrate to Azure Database for PostgreSQL using dump and restore](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore/)<br>
* [Reaching the storage limit](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#reaching-the-storage-limit)
* [Scaling resources in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#scale-resources/)<br>
* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
