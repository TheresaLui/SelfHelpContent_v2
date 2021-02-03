<properties
  pagetitle="Creating, scaling, and deleting an Azure Database for MySQL server"
  description="Creating, scaling, and deleting an Azure Database for MySQL server"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,pariks"
  selfhelptype="Generic"
  supporttopicids="32747557"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="5fc3807b-cdfa-44cf-807b-1b104f13b6a9"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Creating, scaling, and deleting an Azure Database for MySQL server

You can manage databases in Azure Database for MySQL servers through the ARM template by using the Azure CLI and by calling our REST APIs. 

**Note:** Most of the management operations are asynchronous. You might need to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve issues encountered during these processes by using the following steps.

## **Recommended Steps**

* In Azure Database for MySQL, the [`mysql` system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only because it is used to support various PaaS service functionalities. **Note:** You cannot change anything in the `mysql` system database.
* `Charset` and `collation` are the only database properties that are supported in current framework. For more information, see [Supported charset and collation](https://dev.mysql.com/doc/refman/8.0/en/charset-charsets.html). If you want to change other properties during database creation or update, connect to MySQL by using a client such as Azure CLI and execute [`CREATE DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/creating-database.html) or [`ALTER DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/alter-database.html).
* To learn how to use ARM templates to create databases in Azure Database for MySQL server, see [Create databases in Azure Database for MySQL](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithDatabase) ARM template.
* **Note:** "Update databases" is not an available option in the ARM Template. Make sure that the `charset` and `collation` properties for a database stay the same when you rerun the deployment.

* If you're using Azure CLI:

  * Make sure you are signed in correctly, using **az login**
  * Make sure you're using the correct subscription, in case you have more than one subscription
  * Specify all required parameters in **az mysql server create** with valid values. For required parameters and values, see the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)

* For issues encountered using our REST API, see the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/)

* If you want to create users after the server creation, see [Create databases and users](https://docs.microsoft.com/azure/mysql/howto-create-users?tabs=single-server).

## **Recommended Documents**

* [Azure Database for MySQL servers](https://docs.microsoft.com/azure/mysql/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)<br>
* [Available pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Current known limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
