<properties
    pageTitle="Error while scaling a resource in Azure Database for MySQL Flexible Server"
    description="Error while scaling a resource in Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="350"
    selfHelpType="generic"
    supportTopicIds="32747613"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="98ed92cb-eb30-45ae-b80c-bd02f711fa39"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Error while scaling a resource in Azure Database for MySQL Flexible Server

In Azure Database for MySQL Flexible Server, both compute and storage resources can be scaled. Scaling compute resources (across compute tiers or vCores) requires a server restart to apply. Scaling storage is an online operation and does not require a restart.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Connections are dropped and no new connections can be established while vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MySQL server once the scale operation is completed. Storage scaling does not cause a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

    * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

* The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure runbook and python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177)

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)<br>
* [Azure Database for MySQL Flexible Server - Compute + storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)<br>
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)