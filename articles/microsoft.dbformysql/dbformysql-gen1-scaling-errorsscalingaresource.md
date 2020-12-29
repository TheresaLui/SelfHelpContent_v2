<properties
    pageTitle="Error while scaling a resource in Azure Database for MySQL Single Server"
    description="Error while scaling a resource in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="360"
    selfHelpType="generic"
    supportTopicIds="32747560"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0c67de7c-94e5-4f04-a320-810513a9c87b"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Error while scaling a resource in Azure Database for MySQL Single Server

In Azure Database for MySQL Single Server, both compute and storage resources can be scaled. Scaling pricing tiers can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported. Scaling compute resources (across pricing tiers or vCores) requires a server restart to apply. Scaling storage is an online operation and does not require a restart.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * If you want to switch from Basic to General Purpose or Memory Optimized and vice-versa, please follow the steps in [Upgrade from Basic to General Purpose or Memory Optimized tiers](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/830404) blog

* Connections are dropped and no new connections can be established while vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement [retry logic](https://docs.microsoft.com/azure/mysql/concepts-connectivity) so your application can seamlessly reconnect to the MySQL server once the scale operation is completed. Storage scaling does not cause a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

    * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

* Cannot scale storage provisioned up to 16 TB:

    * Your server may be running on our storage option supporting up to 4 TB. To upgrade your server to support up to 16 TB, perform a dump & restore to a new server created with 16 TB.

* The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure runbook and python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177)

## **Recommended Documents**

* [Azure Database for MySQL Single Server documentation](https://docs.microsoft.com/azure/mysql/single-server)<br>
* [Azure Database for MySQL Single Server - Pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)<br>
* [Read Replicas in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#replica-configuration/)