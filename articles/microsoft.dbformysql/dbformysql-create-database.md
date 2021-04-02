<properties
  pagetitle="Creating, scaling, and deleting an Azure Database for MySQL server&#xD;"
  description="Creating, scaling, and deleting an Azure Database for MySQL server"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="chengxin,jtoland,sumuth"
  selfhelptype="Generic"
  supporttopicids="32684526"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="585c3bad-c062-42e6-8ba2-7173be1383b4"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Creating, scaling, and deleting an Azure Database for MySQL server

You can manage Azure Database for MySQL databases through the ARM template, using the Azure CLI, and by calling our REST APIs. Note that most management operations are asynchronous, so you might have to poll the status of the operation when using Azure CLI or REST APIs.

## Fix it yourself

Resolve any issues by considering and addressing the following points.

* **Azure Portal says MySQL version 5.7 or 8.0, but the application is showing 5.6.47.0**<br>
Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To connect to gateway that is version MySQL 5.7 using port number 3308 instead of 3306 and to connect through gateway that is running MySQL version 8.0 connect via port 3309.

   **Connection string examples:**<br>
  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p<br>
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

* **Issues with deleting a server**<br>
  Check if there is a [DELETE lock](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources#managed-applications-and-locks) on your server preventing you from deleting. Remove the lock and then proceed to delete the server using any one of these steps:
  * Azure portal: Use the **Delete** button in the toolbar on the **Overview** page
  * Azure CLI: Use the command [az mysql server delete](https://docs.microsoft.com/cli/azure/mysql/server?#az_mysql_server_delete) or [az mysql flexible-server delete](https://docs.microsoft.com/cli/azure/mysql/flexible-server?#az_mysql_flexible_server_delete) based on deployment option
  * REST API: use the DELETE operation with valid values

* **Restore a dropped server**<br>
  To recover a dropped MySQL server resource within 5 days from the time of server deletion, follow [this guide](https://docs.microsoft.com/azure/mysql/howto-restore-dropped-server).

* **Issues when using ARM templates**<br>
  To become familiar with using ARM templates to create databases in Azure Database for MySQL server, see [Provision an Azure Database for MySQL server using Azure Resource Manager template](https://docs.microsoft.com/azure/mysql/tutorial-provision-mysql-server-using-azure-resource-manager-templates?tabs=azure-portal) and the [ExampleWithDatabase](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithDatabase) ARM template. Note that **Update databases** is not an available option in the ARM Template. Ensure that the `charset` and `collation` for a database remain the same when you rerun the deployment.

* **Issues when using Azure CLI**<br>
  * Make sure that you're signed in to the correct account by using `az login`.
  * Ensure that you're using the correct subscription, if you have multiple subscriptions.
  * Specify all required parameters in `az mysql server create` using valid values. See [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.
  
* **Issues when using our REST API**<br>
  See [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/).

* **Issues updating MySQL Database Server**<br>
  * In Azure Database for MySQL, the [`mysql` system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only because it's used to support various aspects of PaaS service functionality. Note that you can't change anything in the `mysql` system database.
  * **`Charset`** and **`collation`** are the only database properties supported in the current framework. See [Supported charset and collation](https://dev.mysql.com/doc/refman/8.0/en/charset-charsets.html) for more information. If you want to change other properties during database creation or update, connect to MySQL using a client such as the Azure CLI, and then run [`CREATE DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/creating-database.html) or [`ALTER DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/alter-database.html).

## **Recommended documents**

* [Server concepts](https://docs.microsoft.com/azure/mysql/concepts-servers)
* [Supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)
* [Available pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)
* [Current known limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
