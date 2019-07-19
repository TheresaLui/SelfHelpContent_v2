<properties
    pageTitle="Manage the Azure Database for MySQL using ARM Templates"
    description="ARM template issues for the Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="50"
    selfHelpType="resource"
    supportTopicIds="32640044"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="47d6ebbc-3cec-49ff-89b0-e57ee21f1085"
/>

# Manage the Azure Database for MySQL using ARM Templates

The Azure Database for MySQL REST API enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Familiarize yourself with one of our sample [Azure Resource Manager](https://github.com/Azure/azure-quickstart-templates/tree/master/101-managed-mysql-with-vnet) template in Azure Quickstart GitHub Gallery, compare your template against it, and or build on top of it
* If your deployment is failing:

  * Make sure your the server name is globally unique
  * Required parameters are set and valid. See the [Provisioning Azure Database for MySQL using ARM templates](https://docs.microsoft.com/azure/mysql/tutorial-provision-mysql-server-using-azure-resource-manager-templates#create-an-azure-database-for-mysql-server-with-vnet-service-endpoint-using-azure-resource-manager-template) to understand the valid values of the parameters.
* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.

## **Recommended Documents**

* [Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/)<br>
* [Sample deployment using ARM templates](https://github.com/Azure/azure-mysql/tree/master/arm-templates)<br>
* [Rest API for MySQL](https://docs.microsoft.com/rest/api/mysql/#)<br>
* [Resource types and versions](https://docs.microsoft.com/azure/templates/microsoft.dbformysql/allversions)
