<properties
    pageTitle="Server parameter not listed in Azure Database for MariaDB"
    description="Guidance on what to do when a server parameter is not listed"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32640154"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="a78b942f-009d-4b7b-931a-6cc8c17fff21"
/>

# Server parameter not listed

Azure Database for MariaDB allows you to configure parameters at a server level using the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-server-parameters) or the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-parameters-cli). To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal.

## **Recommended Steps**

* Review the [non-configurable server parameters](https://docs.microsoft.com/azure/mariadb/howto-server-parameters#non-configurable-server-parameters).
* To change the **time_zone* parameter, follow the [instruction](https://docs.microsoft.com/azure/mariadb/howto-server-parameters#working-with-the-time-zone-parameter) to populate the time zone table.
* Review the [server parameter limitation](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas#considerations-and-limitations) for read replica server.
* The [read replicas](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas) has **read_only = ON**, and we don't support to change it.
* To change the in **read_only** parameter for non read replicas, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers#storage).
* If a parameter you'd like to configure is not listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/915439-azure-database-for-mariadb)

## **Recommended Documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/mariadb/howto-server-parameters/)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-parameters-cli/)
