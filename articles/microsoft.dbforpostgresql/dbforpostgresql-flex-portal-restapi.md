<properties
    pageTitle="Design, Development, and APIs for PostgreSQL - REST and ARM template"
    description="Design, Development, and APIs for PostgreSQL - REST and ARM template"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="380"
    selfHelpType="generic"
    supportTopicIds="32780898"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-portal-restapi"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Using Azure REST APIs and ARM templates for Azure Database for PostgreSQL

Azure Database for PostgreSQL management operations can be performed using REST APIs.

## **Recommended Steps**

* If you want to know whether a specific command is supported, or which parameters are required, or to see samples on how to use a command, see our [REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/)
* If you are using Azure Resource Manager templates and have an issue:
    * To familiarize yourself with Azure Resource Manager templates, create a sample template by clicking on **Export Template** in the portal for an existing Azure Database for PostgreSQL
    * Confirm that required parameters are set and valid. See [Azure Database for PostgreSQL REST API](https://docs.microsoft.com/rest/api/postgresql/) to understand the valid values of the parameters.

* Poll the status of the operation after you issue the request. Most operations are asynchronous and can take several minutes to complete.
* Attempting to delete a component by removing its mention from the ARM template (complete mode deletion) is not supported. For more information, see [complete mode deletion](https://docs.microsoft.com/azure/azure-resource-manager/complete-mode-deletion).
* To move a server across resource groups or subscriptions, see [Azure resource move](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)

