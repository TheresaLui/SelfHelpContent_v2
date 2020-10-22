<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MySQL Flexible Server"
    description="Creating, scaling, and deleting an Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32747636"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7a698dd8-9a13-45da-86eb-5a1f4373b650"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Creating, scaling, and deleting an Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible Servers can be managed through the Azure portal, Azure CLI, REST APIs, or ARM templates. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you may have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Issues with creating a server*

* Servers can be created using the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-server-portal), [Azure CLI](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-server-cli), [ARM templates](https://docs.microsoft.com/azure/mysql/mysql/flexible-server/quickstart-create-arm-template), and [REST API](https://docs.microsoft.com/rest/api/mysql/)
* If your server create operation is failing, make sure the server name is globally unique
* If you are experiencing issues with creating your server using the Azure CLI:

  * Make sure you are signed-in to the correct using `az login`
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters for the `az mysql flexible-server create` command. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.
* MySQL versions supported: 5.7

*Issues with updating a server*

* Once your server is created, you can scale the compute size and storage provisioned using the below:
    * Azure portal: use the **Compute + storage** page to scale your resources. Review the [manage a flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal) how-to for more info
    * Azure CLI: use the `az mysql flexible-server update` command with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for more info.
    * REST API: use the `PATCH` operation  with valid values. Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) for more.
* The [mysql system database](https://dev.mysql.com/doc/refman/5.7/en/system-schema.html) is read-only and is used to support various PaaS functionality. You cannot change anything in the `mysql` system database.

*Issues with deleting a server*

* Check if there is an existing [resource lock](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources) on your server preventing you from deleting
* Azure portal: use the **Delete** button in the toolbar on the Overview page
* Azure CLI: use the `az mysql flexible-server delete` command with valid values
* REST API: use the `DELETE` operation with valid values

## **Recommended Documents**

* [Azure CLI reference](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)<br>
* [REST API reference](https://docs.microsoft.com/rest/api/mysql/)<br>
* [Azure Database for MySQL Flexible Servers](https://docs.microsoft.com/azure/mysql/flexible-server/overview)<br>
* [Current known limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)