<properties
    pageTitle="Scaling Azure Database for MySQL servers"
    description="Scaling Azure Database for MySQL servers"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32640086"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d980b014-1500-4f79-a025-03717b4576da"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Scaling Azure Database for MySQL servers

In Azure Database for MySQL, scaling can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * If you want to switch from Basic to General purpose or Memory Optimized and vice-versa, please follow the steps in [Upgrade from Basic to General Purpose or Memory Optimized tiers in Azure Database for MySQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/830404) blog

* Connections are dropped and no new connections can be established while vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MySQL server once the scale operation is completed. Storage scaling does not cause a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

    * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

* Scaling fails with error "Service is temporarily busy and the operation cannot be performed. Please try again later":

    * Try to scale the server again after a few minutes have passed

* The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure runbook and Python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Migrate to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)
* [Scaling resources in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#scale-resources/)
