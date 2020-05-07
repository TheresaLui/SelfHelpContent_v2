<properties
    pageTitle="Design, Development, and APIs for MySQL - REST"
    description="Design, Development, and APIs for MySQL - REST"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="330"
    selfHelpType="generic"
    supportTopicIds="32640088"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="bdff2bb9-1323-472a-973b-b3f2675fdd83"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Using Azure REST APIs for Azure Database for MySQL

All Azure Database for MySQL management operations can be performed using REST APIs.

## **Recommended Steps**

* If you are looking if a specific command is supported, samples on how to use a command, or which parameters are required, please refer to our [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/)
* If you are using Azure Resource Manager templates and have a issue:

    * Familiarize yourself with one of our sample [Azure Resource Manager](https://github.com/Azure/azure-quickstart-templates/tree/master/101-managed-mysql-with-vnet) template in Azure Quickstart GitHub Gallery, compare your template against it, and or build on top of it
    * Ensure the required parameters are set and valid. See the [Provisioning Azure Database for MySQL using ARM templates](https://docs.microsoft.com/azure/mysql/tutorial-provision-mysql-server-using-azure-resource-manager-templates#create-an-azure-database-for-mysql-server-with-vnet-service-endpoint-using-azure-resource-manager-template) to understand the valid values of the parameters.

* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.
* To learn how to move a server across resource groups or subscriptions, review [Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)


## **Recommended Documents**

* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)<br>
* [Rest API for MySQL](https://docs.microsoft.com/rest/api/mysql/)<br>
* [Resource types and versions](https://docs.microsoft.com/azure/templates/microsoft.dbformysql/allversions)
