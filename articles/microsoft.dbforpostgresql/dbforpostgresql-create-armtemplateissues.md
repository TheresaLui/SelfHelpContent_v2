<properties
    pageTitle="Manage Azure Database for PostgreSQL using ARM Templates"
    description="Manage Azure Database for PostgreSQL using ARM Templates"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="260"
    selfHelpType="generic"
    supportTopicIds="32639966"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="b3e8194d-233c-43f3-99cd-9fba9ae792c5"
    />

# Manage Azure Database for PostgreSQL using ARM Templates

The Azure Database for PostgreSQL REST API enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* To familiarize yourself with Azure Resource Manager templates, create a sample template by clicking on **Export Template** in the portal for an existing Azure Database for PostgreSQL server
* If your deployment is failing:
  * Make sure your the server name is globally unique
  * Required parameters are set and valid. See the [Azure Database for PostgreSQL REST API](https://docs.microsoft.com/rest/api/postgresql) to understand the valid values of the parameters.
* Poll the status of the operation after you issue the request. Most operations are asynchronous and can take a few minutes to complete.

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/)<br>
* [Rest API for PostgreSQL](https://docs.microsoft.com/rest/api/postgresql/#)<br>
* [Resource types and versions](https://docs.microsoft.com/azure/templates/microsoft.dbforpostgresql/allversions)
