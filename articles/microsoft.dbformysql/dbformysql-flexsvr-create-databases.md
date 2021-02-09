<properties
  pagetitle="Creating, scaling, and deleting an Azure Database for MySQL Flexible server&#xD;"
  description="Creating, scaling, and deleting an Azure Database for MySQL Flexible server"
  service="microsoft.dbformysql"
  resource="flexibleservers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32747609"
  resourcetags="servers,databases"
  productpesids="17344"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="5eb4c98c-f1f0-43e4-88bf-3c11bc45c873"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Creating, scaling, and deleting an Azure Database for MySQL Flexible server

Databases in Azure Database for MySQL Flexible servers (Preview) can be managed through the ARM template, Azure CLI , Azure portal and REST APIs. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Resolve any issues by considering the following points.

### Considerations

* In Azure Database for MySQL, the [`mysql` system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only because it's used to support various aspects of PaaS service functionality. Note that you can't change anything in the `mysql` system database.
* `Charset` and `collation` are the only database properties supported in current framework. See [Supported `charset` and `collation`](https://dev.mysql.com/doc/refman/8.0/en/charset-charsets.html) for more information.
* To change other properties during database creation or update, connect to MySQL using a client such as `mysql.exe` or MySQL Workbench, and the execute [`CREATE DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/creating-database.html) or [`ALTER DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/alter-database.html)
* If you're using the Azure CLI:

    * See [database-related CLI commands](https://docs.microsoft.com/cli/azure/mysql/db?view=azure-cli-latest) to become familiar with using the CLI to create databases in Azure Database for MySQL.
    * Make sure you are signed in to the correct account by using **az login**.
    * Ensure that you are using the correct subscription if you have multiple subscriptions.
    * Specify all required parameters in **`az mysql server create`** using valid values. See the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.

* See the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) if you encounter issues using our REST API.
* If you're using ARM templates, **Update databases** is not an available option. Make sure that `charset` and `collation` for a database remain the same when you rerun the deployment.

## **Recommended documents**

* [Azure Database for MySQL Flexible servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-servers)
* [Supported versions](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-supported-versions)
* [Available compute tiers and storage size](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)
* [Current know limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)
