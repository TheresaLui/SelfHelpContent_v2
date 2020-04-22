<properties
    pageTitle="Server Parameters in Azure Database for MySQL"
    description="Server parameter not listed"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="450"
    selfHelpType="generic"
    supportTopicIds="32640092"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6145858c-683d-49dd-b4c8-f10f2d2a2f3c"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Server parameter not listed

Azure Database for MySQL allows you to configure parameters at a server level using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters) or the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli). To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal.

## **Recommended Steps**

* Review the [non-configurable server parameters](https://docs.microsoft.com/azure/mysql/howto-server-parameters#non-configurable-server-parameters)
* To change the **time_zone** parameter, follow the [instructions](https://docs.microsoft.com/azure/mysql/howto-server-parameters#working-with-the-time-zone-parameter) to populate the time zone table
* Review the [server parameter limitations](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#considerations-and-limitations) for read replica server
* The [read replicas](https://docs.microsoft.com/azure/mysql/concepts-read-replicas) has **read_only = ON**, and we don't support to change it
* To change the in **read_only** parameter for non read replicas, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage)
* If a parameter you'd like to configure is not listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597982-azure-database-for-mysql)
* In the service, a gateway is used to redirect the connections to server instances. After the connection is established, the MySQL client displays the version of MySQL set in the gateway, not the actual version running on your MySQL server instance. To determine the version of your MySQL server instance, use the `SELECT VERSION();` command at the MySQL prompt. See [more details](https://docs.microsoft.com/azure/mysql/concepts-supported-versions).
* Plugin installation is not supported
* If you want to migrate the database to Azure, check the [migration instruction](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)
* To change session level parameter in MySQL for each new connection you can set it through init_connect. Refer to [server parameter setting](https://docs.microsoft.com/azure/mysql/howto-server-parameters) how-to.

## **Recommended Documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli)
