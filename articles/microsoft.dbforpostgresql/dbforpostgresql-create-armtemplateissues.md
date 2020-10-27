<properties
    pageTitle="Manage Azure Database for PostgreSQL using ARM Templates and REST API"  
    description="Manage Azure Database for PostgreSQL using ARM Templates and REST API"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="260"
    selfHelpType="generic"
    supportTopicIds="32639966, 32780989"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b3e8194d-233c-43f3-99cd-9fba9ae792c5"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Manage Azure Database for PostgreSQL using ARM Templates and REST API

The Azure Database for PostgreSQL REST API enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If your deployment is failing:
  * If you are creating a new server, make sure the server name is globally unique
  * If you are deploying or updating multiple server attributes (including firewall rules, Virtual Network rules, server parameters or databases) for a given server, make sure you are deploying these serially. Deploying in parallel will cause a failure. Familiarize yourself with [Sample ARM templates](https://github.com/Azure/azure-postgresql/tree/master/arm-templates/ExampleWithMultipleServerProperties) for examples.
  * Required parameters are set and valid. See the [Azure Database for PostgreSQL REST API](https://docs.microsoft.com/rest/api/postgresql) to understand the valid values of the parameters.
* Poll the status of the operation after you issue the request. Most operations are asynchronous and can take a few minutes to complete.

## **Recommended Documents**

* [Create databases in Azure Database for PostgreSQL](https://github.com/Azure/azure-postgresql/tree/master/arm-templates/ExampleWithDatabase)<br>
* [Create Azure Database for PostgreSQL with multiple firewall rules](https://github.com/Azure/azure-postgresql/tree/master/arm-templates/ExampleWithFirewallRule)<br>
* [Deploy Azure Database for PostgreSQL with CanNotDelete lock](https://github.com/Azure/azure-postgresql/tree/master/arm-templates/ExampleWithLocks)