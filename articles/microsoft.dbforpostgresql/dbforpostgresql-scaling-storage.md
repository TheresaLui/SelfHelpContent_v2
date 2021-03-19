<properties
    pageTitle="Error while scaling a resource in Azure Database for PostgreSQL"
    description="Error while scaling a resource in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32790087"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="661045d6-ccc1-4432-8e62-4fb03c4fdf3e"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Scaling storage Azure Database for PostgreSQL

Most customers see the size of the database grow overtime. Single Server allows customers to provision the storage based on initial size of the database and the projected data growth. The storage can dynamically be scaled up online with no impact to the application. A recommended best practice is to enable storage auto-grow. Note, you cannot scale down the storage.

## **Recommended Steps**

* Is scaling of storage a online operation?

    Yes, storage can be scaled up online with no impact to the application. 

* Can I scale IOPS (IOs per second) without scaling up the storage? 

    No, IOPS are strictly tied to the provisioned storage. You will need to scale the storage to achieve the IOPS required.
 
* Can I scale the storage down?

    No, you cannot scale the storage down because it is not supported in community based postgreSQL engine

* Did you find out that your server is set to read only? Are you getting an error saying that your storage is almost full? 

    Single Server automatically switches to read-only when storage is almost full to keep it available for queries. When this occurs, you can either increase the size of provisioned storage, or start a new read-write session and delete non-essential data to free storage. See [thresholds when server is set to read-only and steps to unlock writes](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#reaching-the-storage-limit). We recommend enabling [storage auto-grow](https://docs.microsoft.com/azure/postgresql/howto-auto-grow-storage-portal) to avoid disruption to your application.

* Are you attempting to scale storage beyond 4 TB and can't do it?
 
    Your server is on a legacy storage option tha can't be extended beyond 4 TB. All newly created Single Servers automatically use the large storage (16 TB) if the region supports it. You will need to create a new PostgreSQL Server and then use pg_dump/pg_restore to migrate the data from the old server. Note, you can't do this using point-in-time restore because the storage is incompatible. Please refer to [list of regions](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers) supporting large storage. 

* Are you trying to use the Azure Monitor auto-scale feature with Azure Database for PostgreSQL - Single server? 

    Azure Monitor auto-scale feature is not supported for Azure Database for PostgreSQL - Single server. However, you can configure auto-scaling using Azure run books. See [How to auto-scale an Azure Database for PostgreSQL/MySQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**
* [Azure Postgres compute and storage tiers](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)<br>
* [Read Replica in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#replica-configuration/)<br>
* [Azure Database for PostgreSQL Pricing Page](https://azure.microsoft.com/pricing/details/postgresql/)