<properties
    pageTitle="Manage the Azure Database for MariaDB using ARM Templates"
    description="Manage the Azure Database for MariaDB using ARM Templates"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="240"
    selfHelpType="generic"
    supportTopicIds="32640111"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec" 
    articleId="5c807c9b-3605-4ec4-8942-feed80629bc0"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Manage the Azure Database for MariaDB using ARM Templates

The Azure Database for MariaDB REST API enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If your deployment is failing:
    
  * If you are creating a new server, make sure your the server name is globally unique
  * If you are deploying or updating multiple server attributes which includes firewall rules, Virtual Network rules, server parameters or databases for a given server, make sure you are deploying these serially, in any order. Familiarize yourself with [Sample ARM templates](https://github.com/Azure/azure-mariadb/tree/master/arm-templates/ExampleWithMultipleServerProperties)
  * Required parameters are set and valid. See the [Azure Database for MariaDB REST API](https://docs.microsoft.com/rest/api/mariadb) to understand the valid values of the parameters.
* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.

## **Recommended Documents**

* [Create databases in Azure Database for MariaDB](https://github.com/Azure/azure-mariadb/tree/master/arm-templates/ExampleWithDatabase)<br>
* [Deploy Azure Database for MariaDB with CanNotDelete lock](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithLocks)<br>
* [Create Azure Database for MariaDB with multiple firewall rules](https://github.com/Azure/azure-mariadb/tree/master/arm-templates/ExampleWithFirewallRule)
