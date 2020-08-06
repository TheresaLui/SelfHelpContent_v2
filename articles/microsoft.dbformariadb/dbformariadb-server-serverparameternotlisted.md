<properties
    pageTitle="Server parameter in Azure Database for MariaDB"
    description="Server parameter not listed"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32640154"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a78b942f-009d-4b7b-931a-6cc8c17fff21"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Server parameter not listed

Azure Database for MariaDB allows you to configure parameters at a server level using the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-server-parameters) or the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-parameters-cli). To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal.

## **Recommended Steps**

* Review the [non-configurable server parameters](https://docs.microsoft.com/azure/mariadb/concepts-server-parameters#non-configurable-server-parameters)
* To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (ex. `log_bin_trust_function_creators`,`innodb_file_per_table` are locked on both master and replica). Refer to [documentation](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas#server-parameters) for the list of parameters that are locked. To update one of the locked parameters on the master server, please delete replica servers, update the parameter value on the master, and recreate replicas.
* If the server parameter you want to update is not listed in the Azure portal, you can optionally set the parameter at the connection level using **init_connect**. Refer to [setting parameter not listed](https://docs.microsoft.com/azure/mariadb/howto-server-parameters#setting-parameters-not-listed)
* To change the **time_zone** parameter, follow the [instructions](https://docs.microsoft.com/azure/mariadb/howto-server-parameters#working-with-the-time-zone-parameter) to populate the time zone table
* Review the [server parameter limitation](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas#considerations-and-limitations) for read replica server
* The [read replicas](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas) has **read_only = ON**, and we don't support changing it
* To change the in **read_only** parameter for non read replicas, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers#storage)
* If a parameter you'd like to configure is not listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/915439-azure-database-for-mariadb)
* In the service, a gateway is used to redirect the connections to server instances. After the connection is established, the MariaDB client displays the version of MariaDB set in the gateway, not the actual version running on your MariaDB server instance. To determine the version of your MariaDB server instance, use the `SELECT VERSION();` command at the MariaDB prompt. See [more details](https://docs.microsoft.com/azure/mariadb/concepts-supported-versions).
* Plugin installation is not supported
* If you want to migrate the database to Azure, check the [migration instruction](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore/)

## **Recommended Documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/mariadb/howto-server-parameters/)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-parameters-cli/)
