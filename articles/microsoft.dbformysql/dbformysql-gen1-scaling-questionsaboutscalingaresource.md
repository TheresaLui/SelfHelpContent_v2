<properties
    pageTitle="Scaling Azure Database for MySQL Single Server"
    description="Scaling Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="380"
    selfHelpType="generic"
    supportTopicIds="32747579"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9ee450f6-7d42-4cf1-a777-a8bd8e576e61"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Scaling Azure Database for MySQL Single Server

In Azure Database for MySQL Single Server, scaling can be done for both compute and storage resources. Scaling operations can be done from the Azure portal, Azure CLI, ARM templates, or REST API.

## **Recommended Steps**

*Compute* 

* Scaling between General Purpose and Memory Optimized tiers is supported. Scaling to/from the Basic tier is not supported.

    * If you want to switch from Basic to General purpose or Memory Optimized and vice-versa, please follow the steps in [Upgrade from Basic to General Purpose or Memory Optimized tiers](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/830404) blog

* Connections are dropped and no new connections can be established while pricing tiers or vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MySQL server once the scale operation is completed.

*Storage*

* Scaling storage is an online operation and does not require a server restart.
* Scaling fails with error "Service is temporarily busy and the operation cannot be performed. Please try again later":

    * Try to scale the server again after a few minutes have passed

*Read replicas*

* Cannot scale up the source server when a replica exists, or cannot scale down a replica:

    * Before a source server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the source.

The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure runbook and Python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Azure Database for MySQL Single Server - Pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)<br>
* [Migrate to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)