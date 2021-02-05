<properties
  pagetitle="Creating, scaling, and deleting an Azure Database for MySQL server&#xD;"
  description="Creating, scaling, and deleting an Azure Database for MySQL server"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="chengxin,jtoland"
  selfhelptype="Generic"
  supporttopicids="32684526"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="585c3bad-c062-42e6-8ba2-7173be1383b4"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Creating, scaling, and deleting an Azure Database for MySQL server

You can manage Azure Database for MySQL databases through the ARM template, using the Azure CLI, and by calling our REST APIs. Note that most management operations are asynchronous, so you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users can resolve their issues by considering and addressing the following points.

### Considerations

* In Azure Database for MySQL, the [mysql system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only as it's used to support various aspects of PaaS service functionality. Note that you cannot change anything in the mysql system database.
* **Charset** and **collation** are the only database properties supported in the current framework. Refer to [Supported charset and collation](https://dev.mysql.com/doc/refman/8.0/en/charset-charsets.html) for more information. If you want to change other properties during database creation or update, connect to MySQL using a client, such as the Azure CLI and then run [`CREATE DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/creating-database.html) or [`ALTER DATABASE`](https://dev.mysql.com/doc/refman/8.0/en/alter-database.html).
* To familiarize yourself with using ARM templates to create databases in Azure Database for MySQL server, refer to [Provision an Azure Database for MySQL server using Azure Resource Manager template](https://docs.microsoft.com/azure/mysql/tutorial-provision-mysql-server-using-azure-resource-manager-templates?tabs=azure-portal) and the [ExampleWithDatabase](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithDatabase) ARM template. Note that **Update databases** is not an available option in the ARM Template. Ensure that the `charset` and `collation` for a database remain the same when you rerun the deployment.

* If you're using Azure CLI:

  * Make sure that you're signed-in to the correct account by using `az login`.
  * Ensure you are using the correct subscription if you have multiple subscriptions.
  * Specify all required parameters in `az mysql server create` using valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.
  
* If you encounter issues using our REST API, consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) 

## **Recommended documents**

* [Server concepts](https://docs.microsoft.com/azure/mysql/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)<br>
* [Available pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Current known limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
