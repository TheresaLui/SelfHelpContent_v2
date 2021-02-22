<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for PostgreSQL server"
    description="Creating, scaling, and deleting an Azure Database for PostgreSQL server"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="210"
    selfHelpType="generic"
    supportTopicIds="32640024, 32780997"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8fff8916-841c-4a25-9116-773f962399ff"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Creating, scaling, and deleting an Azure Database for PostgreSQL server

[!Note]
- **Due to ongoing COVID 19, we have mobilized our global response plan to help customers and partners stay up and running during this critical time. We are actively monitoring performance and usage trends 24/7 to ensure we are optimizing our services for customers worldwide, while accommodating this significant new demand.**

- **We have established clear criteria for prioritizing new cloud capacity if needed – top priority will be going to first responders, health and emergency management services, critical government infrastructure, and ensuring remote workers stay up and running with the core functionality of Teams.**

- **We appreciate that these can raise questions, so we have tried to address the most common ones in our [recent blog post](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity).**


Azure Database for PostgreSQL servers can be managed through the Azure portal, using the Azure CLI, and by calling our REST APIs. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Make sure that the server name is globally unique
* Automatic major version upgrade is not supported. For example, there is not an automatic upgrade from PostgreSQL 9.5 to PostgreSQL 9.6. To upgrade to the next major version, create a [database dump and restore](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore) to a server that was created with the new engine version.
* If you are using the portal, review the [Manage an Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal) how-to
* If you are using Azure CLI:

  * Make sure you are signed-in to the correct account using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az postgres** with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest) for required parameters and valid values.
  
* Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/) if you encounter issues using our REST

## **Recommended Documents**

* [Azure Database for PostgreSQL servers](https://docs.microsoft.com/azure/postgresql/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/postgresql/concepts-supported-versions)<br>
* [Compute and storage options](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)<br>
* [Limits](https://docs.microsoft.com/azure/postgresql/concepts-limits)
