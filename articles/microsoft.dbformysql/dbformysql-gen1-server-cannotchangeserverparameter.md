<properties
    pageTitle="Server parameter not listed"
    description="Server parameter not listed"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna,jtoland"
    displayOrder="430"
    selfHelpType="generic"
    supportTopicIds="32747550"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1e6e66c0-4e0e-4d02-926b-0d96c1d9ea65"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Server parameter not listed

Azure Database for MySQL Single Server allows you to configure parameters at a server level using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters) or the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli). To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal.

> [!NOTE]
> The server parameter `enforce_gtid_consistency` was configured to ON to help with avoiding unexpected issues after enabling GTID in the future. In some cases transaction may violate the GTID consistency and you may experience issues blocking your workload with an error like "ERROR: Statement violates GTID consistency".<br>
If you do not want to enforce GTID, please contact support or our team at AskAzureDBforMySQL@service.microsoft.com with your subscription ID & server name and we will help update the parameter.

## Fix it yourself

* Review the [non-configurable server parameters](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#non-configurable-server-parameters).
* To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (ex. `log_bin_trust_function_creators`,`innodb_file_per_table` are locked on both master and replica). Refer to [documentation](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters) for the list of parameters that are locked. To update one of the locked parameters on the master server, please delete replica servers, update the parameter value on the master, and recreate replicas.
* If the server parameter you want to update is not listed in the Azure portal, you can optionally set the parameter at the connection level using **init_connect**. Refer to [setting parameter not listed](https://docs.microsoft.com/azure/mysql/howto-server-parameters#setting-parameters-not-listed).
* To change the **time_zone** parameter, follow the [instructions](https://docs.microsoft.com/azure/mysql/howto-server-parameters#working-with-the-time-zone-parameter) to populate the time zone table.
* Review the [server parameter limitations](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#considerations-and-limitations) for read replica server.
* The [read replicas](https://docs.microsoft.com/azure/mysql/concepts-read-replicas) has **read_only = ON**, and we don't support changing it.
* To change the **read_only** parameter for non read replicas, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage).
* If a parameter you'd like to configure isn't listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597982-azure-database-for-mysql).
* To update server parameters globally at the server-level, use the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli), [PowerShell](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-powershell), or [Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters).
* In the service, a gateway is used to redirect the connections to server instances. After the connection is established, the MySQL client displays the version of MySQL set in the gateway, not the actual version running on your MySQL server instance. To determine the version of your MySQL server instance, use the `SELECT VERSION();` command at the MySQL prompt. See [more details](https://docs.microsoft.com/azure/mysql/concepts-supported-versions).
* Plugin installation is not supported.
* If you want to migrate the database to Azure, check the [migration instruction](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/).
* **Azure Portal says MySQL version 5.7 or 8.0, but the application is showing 5.6.47.0**<br>
Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To connect to gateway that is version MySQL 5.7 using port number 3308 instead of 3306 and to connect through gateway that is running MySQL version 8.0 connect via port 3309.

   **Connection string examples:**<br>
  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

## **Recommended documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli)