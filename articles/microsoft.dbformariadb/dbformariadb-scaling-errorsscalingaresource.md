<properties
    pageTitle="Error while scaling a resource in Azure Database for MariaDB"
    description="Error while scaling a resource in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="170"
    selfHelpType="generic"
    supportTopicIds="32640119"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="50905891-e140-4f61-a758-41493777c12d"
    	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Error while scaling a resource in Azure Database for MariaDB

In Azure Database for MariaDB, scaling can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * If you want to switch from Basic to General Purpose or Memory Optimized and vice-versa, please follow the steps in [Upgrade from Basic to General Purpose or Memory Optimized tiers in Azure Database for MariaDB](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/830404) blog

* Connections are dropped and no new connections can be established while vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MariaDB server once the scale operation is completed. Storage scaling does not cause a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

    * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

* The Azure Monitor auto-scale feature is not supported in Azure Database for MariaDB

## **Recommended Documents**

* [Azure Database for MariaDB Pricing Page](https://azure.microsoft.com/pricing/details/mariadb/)<br>
* [Read Replica in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas#replica-configuration/)
