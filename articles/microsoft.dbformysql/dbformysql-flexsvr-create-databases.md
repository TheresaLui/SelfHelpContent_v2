<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MySQL Flexible server"
    description="Creating, scaling, and deleting an Azure Database for MySQL Flexible server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="mksuni"
    ms.author="sumuth"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32747609"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5eb4c98c-f1f0-43e4-88bf-3c11bc45c873"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Creating, scaling, and deleting an Azure Database for MySQL Flexible server

Databases in Azure Database for MySQL Flexible servers (Preview) can be managed through the ARM template, Azure CLI , Azure portal and REST APIs. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* In Azure Database for MySQL, the [mysql system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only as it is used to support various PaaS service functionality. Please note that you cannot change anything in the `mysql` system database.
* Charset and collation are the only database properties that are supported in current framework. Please refer to [Supported charset and collation](https://dev.mysql.com/doc/refman/8.0/en/charset-charsets.html) for more information.
* If you would like to change other properties during database creation or update, connect to MySQL using a client like mysql.exe or MySQL Workbench and execute [CREATE DATABASE](https://dev.mysql.com/doc/refman/8.0/en/creating-database.html) or [ALTER DATABASE](https://dev.mysql.com/doc/refman/8.0/en/alter-database.html)
* If using Azure CLI:

    * To familiarize yourself with using CLI to create databases in Azure Database for MySQL[database related CLI commands](https://docs.microsoft.com/cli/azure/mysql/db?view=azure-cli-latest)
    * Make sure you are signed-in to the correct using **az login**
    * Ensure you are using the correct subscription, in case you have more than one
    * Specify all required parameters in **az mysql server create** with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.

* Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) if you encounter issues using our REST API
* If using ARM templates, "Update databases" is not an available option. Please make sure charset and collation for a database stay the same when you rerun the deployment.

## **Recommended Documents**

* [Azure Database for MySQL Flexible servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-supported-versions)<br>
* [Available compute tiers and storage size](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)<br>
* [Current know limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)
