<properties
    pageTitle="Scaling Azure Database for MySQL Flexible Server"
    description="Scaling Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="370"
    selfHelpType="generic"
    supportTopicIds="32747631"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3f38dbc0-4389-414c-b27c-6186bbf0bb11"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Scaling Azure Database for MySQL Flexible Server

In Azure Database for MySQL Flexible Server, scaling can be done for both compute and storage resources. Scaling operations can be done from the Azure portal, Azure CLI, ARM templates, or REST API.

## **Recommended Steps**

*Compute*

* Scaling between all compute tiers and sizes is supported

* Connections are dropped and no new connections can be established while compute tiers or sizes are scaled:

    * Compute tier and size scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MySQL server once the scale operation is completed.

*Storage*

* Scaling storage is an online operation and does not require a server restart

* Scaling fails with error "Service is temporarily busy and the operation cannot be performed. Please try again later":

    * Try to scale the server again after a few minutes have passed

*Read replicas*

* Cannot scale up the source server when a replica exists, or cannot scale down a replica:

    * Before a source server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the source.

The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure runbook and Python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Azure Database for MySQL Flexible Server - Compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)<br>
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)<br>
* [Migrate to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)