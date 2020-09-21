<properties
    pageTitle="Manage the Azure Database for MySQL Single Server using ARM Templates"
    description="Manage the Azure Database for MySQL Single Server using ARM Templates"
    service="microsoft.dbformysql"
    resource="servers"
    authors="mksuni"
    ms.author="sumuth"
    displayOrder="120"
    selfHelpType="generic"
    supportTopicIds="32747540"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fcd2b21e-9307-4ef7-8414-931f9d9a8de8"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Manage the Azure Database for MySQL Single Server using ARM Templates

The Azure Database for MySQL Single Server REST APIs enables you to automate the management of servers in Azure. Note that most of the management operations are asynchronous and you might have to poll the status of the operation if using REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* You can [troubleshoot common issues with ARM template deployments](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-troubleshoot)
* If you are creating a new server, make sure your the server name is globally unique
* If you are deploying or updating multiple server attributes which includes firewall rules, Virtual Network rules, server parameters or databases for a given server, make sure you are deploying these serially, in any order. By default, ARM deploys resources in parallel and a deployment may fail if configured in parallel. Familiarize yourself with [Sample ARM templates](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithMultipleServerProperties).
* Required parameters are set and valid. See the [Provisioning Azure Database for MySQL using ARM templates](https://docs.microsoft.com/azure/mysql/tutorial-provision-mysql-server-using-azure-resource-manager-templates#create-an-azure-database-for-mysql-server-with-vnet-service-endpoint-using-azure-resource-manager-template) to understand the valid values of the parameters.
* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.

## **Recommended Documents**

* [Create databases in Azure Database for MySQL](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithDatabase)<br>
* [Create Azure Database for MySQL with multiple firewall rules](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithFirewallRule)<br>
* [Create Azure Database for MySQL with virtual network rules](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithVirtualNetworkRules)<br>
* [Troubleshoot ARM template deployments](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-troubleshoot)<br>
