<properties
    pageTitle="Manage the Azure Database for MariaDB using ARM Templates"
    description="Manage the Azure Database for MariaDB using ARM Templates"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="240"
    selfHelpType="resource"
    supportTopicIds="32640111"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="5c807c9b-3605-4ec4-8942-feed80629bc0"
/>

# Manage the Azure Database for MariaDB using ARM Templates

The Azure Database for MariaDB REST API enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* To familiarize yourself with Azure Resource Manager templates, create a sample template by clicking on **Export Template** in the portal for an existing Azure Database for MariaDB
* If your deployment is failing:
    
    * Make sure your the server name is globally unique
    * Required parameters are set and valid. See the [Azure Database for MariaDB REST API](https://docs.microsoft.com/rest/api/mariadb) to understand the valid values of the parameters.
  
* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.

## **Recommended Documents**

* [Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/)<br>
* [Rest API for MariaDB](https://docs.microsoft.com/rest/api/mariadb/)<br>
* [Resource types and versions](https://docs.microsoft.com/azure/templates/microsoft.dbformariadb/allversions)
