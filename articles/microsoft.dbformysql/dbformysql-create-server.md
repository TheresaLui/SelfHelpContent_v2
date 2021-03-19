<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MySQL server"
    description="Creating, scaling, and deleting an Azure Database for MySQL server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="200"
    selfHelpType="generic"
    supportTopicIds="32640089"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6b738e5d-8e6e-4fd3-be60-3522d8a20e4a"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Creating, scaling, and deleting an Azure Database for MySQL server

Azure Database for MySQL offers two deployment types - single server and flexible server. Both types of servers can be managed through the Azure portal, Azure CLI, REST APIs, or ARM templates. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you may have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Issues with creating a server*

Servers can be created using the following:

* Azure portal: [Single server](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-portal) | [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-server-portal)
* Azure CLI: [Single server](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli) | [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-server-cli)
* ARM template: [Single server](https://docs.microsoft.com/azure/mysql/quickstart-create-mysql-server-database-using-arm-template?tabs=azure-portal) | [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-arm-template)
* [REST API](https://docs.microsoft.com/rest/api/mysql/)
* If your server create operation is failing, make sure the server name is globally unique
* If you are experiencing issues with creating your server using the Azure CLI:

  * Make sure you are signed-in to the correct using `az login`
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters for the corresponding create command (`az mysql server create` or `az mysql flexible-server create`). Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.

* MySQL versions supported:

	* Single server: 5.6, 5.7, 8.0
	* Flexible server: 5.7

*Issues with updating a server*

Once your server is created, you can scale the compute and storage resources using the below:

* Azure portal: use the single server "Pricing tiers" or flexible server "Compute + storage" page to scale your resources
* Azure CLI: use the corresponding update command (`az mysql server update`or `az mysql flexible-server update`) with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for more info.
* REST API: use the `PATCH` operation  with valid values. Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) for more.
* In single server, minor and major version upgrades aren't supported. For example, upgrading from MySQL 5.6 to MySQL 5.7 isn't supported. If you'd like to upgrade from 5.6 to 5.7, take a [dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore) it to a server that was created with the new MySQL version.
* The [mysql system database](https://dev.mysql.com/doc/refman/5.7/en/system-schema.html) is read-only and is used to support various PaaS functionality. You cannot change anything in the `mysql` system database.

*Issues with deleting a server*

* Check if there is an existing [resource lock](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources) on your server preventing you from deleting
* Azure portal: use the **Delete** button in the toolbar on the Overview page
* Azure CLI: use the corresponding delete command (`az mysql server delete` or `az mysql flexible-server delete`) with valid values
* REST API: use the `DELETE` operation with valid values

*Issues with stopping a server*

* Check if the server is a primary server to a replica or a replica server. You cannot stop the servers which are part of a [replication topology](https://docs.microsoft.com/azure/mysql/concepts-servers#limitations-of-stopstart-operation).
* When the MySQL server is in the stop state, you are only billed for storage being used

## **Recommended Documents**

* [Azure Database for MySQL overview](https://docs.microsoft.com/azure/mysql/overview)<br>
* [Choosing the right MySQL deployment option in Azure](https://docs.microsoft.com/azure/mysql/select-right-deployment-type)<br>
* [Azure CLI reference](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [REST API reference](https://docs.microsoft.com/rest/api/mysql/)
