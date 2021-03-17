<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MySQL Single Server"
    description="Creating, scaling, and deleting an Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32747584"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c7127308-2714-49a8-8c4a-2626198b5b9e"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Creating, scaling, and deleting an Azure Database for MySQL Single Server

Azure Database for MySQL Single Servers can be managed through the Azure portal, Azure CLI, REST APIs, or ARM templates. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you may have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Issues with creating a server*

* Servers can be created using the [Azure portal](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-portal), [Azure CLI](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli), [ARM templates](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-arm-template?tabs=azure-portal), and [REST API](https://docs.microsoft.com/rest/api/mysql/)
* If your server create operation is failing, make sure the server name is globally unique
* If you are experiencing issues with creating your server using the Azure CLI:

  * Make sure you are signed-in to the correct using `az login`
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters for the `az mysql server create` command. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.
* MySQL versions supported: 5.6, 5.7, 8.0

*Issues with updating a server*

* Once your server is created, you can scale the vCores and storage provisioned using the below:
    * Azure portal: use the **Pricing tiers** page to scale your resources. Review the [manage a single server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal) how-to for more info
    * Azure CLI: use the `az mysql server update` command with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for more info.
    * REST API: use the `PATCH` operation  with valid values. Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) for more.
* Currently, minor and major version upgrades aren't supported. For example, upgrading from MySQL 5.6 to MySQL 5.7 isn't supported. If you'd like to upgrade from 5.6 to 5.7, take a [dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore) it to a server that was created with the new MySQL version.
* The [mysql system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only and is used to support various PaaS functionality. You cannot change anything in the `mysql` system database.

*Issues with deleting a server*

* Check if there is an existing [resource lock](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources) on your server preventing you from deleting
* Azure portal: use the **Delete** button in the toolbar on the Overview page
* Azure CLI: use the `az mysql server delete` command with valid values
* REST API: use the `DELETE` operation with valid values

*Issues with stopping a server*

* Check if the server is a primary server to a replica or a replica server. You cannot stop the servers which are part of a [replication topology](https://docs.microsoft.com/azure/mysql/concepts-servers#limitations-of-stopstart-operation).
* When the MySQL server is in the stop state, you are only billed for storage being used

## **Recommended Documents**

* [Azure CLI reference](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [REST API reference](https://docs.microsoft.com/rest/api/mysql/)<br>
* [Azure Database for MySQL Single Servers](https://docs.microsoft.com/azure/mysql/single-server-overview)<br>
* [Current known limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)