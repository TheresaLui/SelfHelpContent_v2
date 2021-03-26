<properties
  pagetitle="Creating, scaling, and deleting an Azure Database for MySQL server&#xD;"
  description="Creating, scaling, and deleting an Azure Database for MySQL server"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,pariks,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747557"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="5fc3807b-cdfa-44cf-807b-1b104f13b6a9"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Creating, scaling, and deleting an Azure Database for MySQL server

You can manage Azure Database for MySQL databases through the ARM template, using the Azure CLI, and by calling our REST APIs. Note that most management operations are asynchronous, so you might have to poll the status of the operation when using the Azure CLI or REST APIs.

Resolve any issues by considering and addressing the following points.

## Considerations

* In Azure Database for MySQL, the [`mysql` system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only as it's used to support various aspects of PaaS service functionality. Note that you can't change anything in the `mysql` system database.
* `Charset` and `collation` are the only database properties supported in current framework. See [Supported charset and collation](https://dev.mysql.com/doc/refman/8.0/en/charset-charsets.html) for more information. If you want to change other properties during database creation or update, connect to MySQL using a client such as the Azure CLI and then execute [`CREATE DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/creating-database.html) or [`ALTER DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/alter-database.html).
* To become familiar with using ARM templates to create databases in Azure Database for MySQL server, see [Provision an Azure Database for MySQL server using Azure Resource Manager template](https://docs.microsoft.com/azure/mysql/tutorial-provision-mysql-server-using-azure-resource-manager-templates?tabs=azure-portal) and the [ExampleWithDatabase](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithDatabase) ARM template. Note that **Update databases** is not an available option in the ARM Template. Ensure that `charset` and `collation` for a database remain the same when you rerun the deployment.

* **Azure Portal says MySQL version 5.7 or 8.0, but the application is showing 5.6.47.0**
Azure Database for MySQL uses a gateway to redirect connections to server instances. After the connection is established, the MySQL client displays the MySQL version set in the gateway, not the version running on your MySQL server instance. To connect to gateway that is version MySQL 5.7 using port number 3308 instead of 3306 and to connect through gateway that is running MySQL version 8.0 connect via port 3309.

  **Connection string examples:**<br>
  * Gateway 5.7: mysql -h servername.mysql.database.azure.com -u username@servername -P 3308 -p<br>
  * Gateway 8.0: mysql -h servername.mysql.database.azure.com -u username@servername -P 3309 -p

* If you're using the Azure CLI:

  * Make sure you are signed-in to the correct account by using **az login**.
  * Ensure you are using the correct subscription if you have multiple subscriptions.
  * Specify all required parameters in **az mysql server create** using valid values. See the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.
  
* If you encounter issues using our REST API, see the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/).

## **Recommended documents**

* [Server concepts](https://docs.microsoft.com/azure/mysql/concepts-servers)
* [Supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)
* [Available pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)
* [Current known limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
