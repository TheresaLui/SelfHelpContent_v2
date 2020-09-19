<properties
    pageTitle="Manage the Azure Database for MySQL using ARM Templates"
    description="ARM template issues for the Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="240"
    selfHelpType="generic"
    supportTopicIds="32640044"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="47d6ebbc-3cec-49ff-89b0-e57ee21f1085"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Manage the Azure Database for MySQL using ARM Templates

The Azure Database for MySQL REST API enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If your deployment is failing:

  * If you are creating a new server, make sure the server name is globally unique
  * If you are deploying or updating multiple server attributes which includes firewall rules, Virtual Network rules, server parameters or databases for a given server, make sure you are deploying these serially, in any order. By default, ARM deploys resources in parallel and a deployment may fail if configured in parallel. Familiarize yourself with [Sample ARM templates](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithMultipleServerProperties).
  * Required parameters are set and valid. See the [Provisioning Azure Database for MySQL using ARM templates](https://docs.microsoft.com/azure/mysql/tutorial-provision-mysql-server-using-azure-resource-manager-templates#create-an-azure-database-for-mysql-server-with-vnet-service-endpoint-using-azure-resource-manager-template) to understand the valid values of the parameters.
* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.

## **Recommended Documents**

* [Create databases in Azure Database for MySQL](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithDatabase)<br>
