<properties
    pageTitle="Using Azure REST APIs for Azure Database for MariaDB"
    description="Using Azure REST APIs for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="TheJY"
    ms.author="jeanyd"
    displayOrder="330"
    selfHelpType="generic"
    supportTopicIds="32640150"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2f78c24d-a4f8-4e7d-a4d6-72cb8a66f01a"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Using Azure REST APIs for Azure Database for MariaDB

All Azure Database for MariaDB management operations can be performed using REST APIs.

## **Recommended Steps**

* If you are looking if a specific command is supported, samples on how to use a command, or which parameters are required, please refer to our [REST API reference documentation](https://docs.microsoft.com/rest/api/mariadb/)

* If you are using Azure Resource Manager templates and have a issue:

    * To familiarize yourself with Azure Resource Manager templates, create a sample template by clicking on **Export Template** in the portal for an existing Azure Database for MariaDB
    * Required parameters are set and valid. See the [Azure Database for MariaDB REST API](https://docs.microsoft.com/rest/api/mariadb) to understand the valid values of the parameters.
  
* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.
* To learn how to move a server across resource groups or subscriptions, review [Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)


## **Recommended Documents**

* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)<br>
* [Rest API for MariaDB](https://docs.microsoft.com/rest/api/mariadb/)<br>
* [Resource types and versions](https://docs.microsoft.com/azure/templates/microsoft.dbformariadb/allversions)
