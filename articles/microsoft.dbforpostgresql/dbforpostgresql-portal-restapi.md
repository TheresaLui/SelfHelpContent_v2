<properties
    pageTitle="Design, Development, and APIs for PostgreSQL - REST and ARM template"
    description="Design, Development, and APIs for PostgreSQL - REST and ARM template"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="380"
    selfHelpType="generic"
    supportTopicIds="32640017, 32780908"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="aecb2aa5-238b-4dce-b992-f7ab8efba288"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Using Azure REST APIs and ARM templates for Azure Database for PostgreSQL

Azure Database for PostgreSQL management operations can be performed using REST APIs.

## **Recommended Steps**

* If you want to know whether a specific command is supported, samples on how to use a command, or which parameters are required, please refer to our [REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/)
* If you are using Azure Resource Manager templates and have an issue:
    * To familiarize yourself with Azure Resource Manager templates, create a sample template by clicking on **Export Template** in the portal for an existing Azure Database for PostgreSQL
    * Confirm that required parameters are set and valid. See the [Azure Database for PostgreSQL REST API](https://docs.microsoft.com/rest/api/postgresql/) to understand the valid values of the parameters.

* Poll the status of the operation after you issues the request. Most operations are asynchronous and can take a few minutes to complete.
* Attempting to delete a component by removing its mention from the ARM template ('complete mode deletion') is not supported. See [this document](https://docs.microsoft.com/azure/azure-resource-manager/complete-mode-deletion) for more information.
* To move a server across resource groups or subscriptions, review [Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)

## **Recommended Documents**

* [Azure Database for PostgreSQL documentation](https://docs.microsoft.com/azure/postgresql/)
