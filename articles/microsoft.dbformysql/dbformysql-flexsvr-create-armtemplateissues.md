<properties
    pageTitle="Manage the Azure Database for MySQL Flexible Server using ARM Templates"
    description="Manage the Azure Database for MySQL Flexible Server using ARM Templates"
    service="microsoft.dbformysql"
    resource="servers"
    authors="mksuni"
    ms.author="sumuth"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32747594"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b0c56abd-2151-4ae1-88f9-92905d18cf4e"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Manage the Azure Database for MySQL Flexible Server using ARM Templates

The Azure Database for MySQL Flexible Server REST APIs enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation if using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* You can [troubleshoot common issues with ARM template deployments](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-troubleshoot)

* If you are creating a new server, make sure your the server name is globally unique

* If you are deploying or updating multiple server attributes which includes firewall rules, Virtual Network rules, server parameters or databases for a given server, make sure you are deploying these serially, in any order. By default, ARM deploys resources in parallel and a deployment may fail if configured in parallel. Familiarize yourself with [Flexible Server ARM Template](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-arm-template#review-the-template).

* Required parameters are set and valid

* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete

## **Recommended Documents**

* [Create databases in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/flexible-server/quickstart-create-arm-template)<br>
* [Troubleshoot ARM template deployments](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-troubleshoot)<br>
* [Troubleshoot common Azure deployment errors with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/templates/common-deployment-errors)
