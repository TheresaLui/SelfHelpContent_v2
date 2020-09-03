<properties
    pageTitle="Design, Development, and APIs for PostgreSQL - CLI"
    description="Design, Development, and APIs for PostgreSQL - CLI"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="350"
    selfHelpType="generic"
    supportTopicIds="32639969"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-portal-azurecli"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Using Azure CLI for Azure Database for PostgreSQL

Azure Database for PostgreSQL supports managing your server using the Azure CLI. Most customers were able to solve the issues with CLI reviewing the recommended steps.

## **Recommended Steps**

* Make sure you are signed-in to the correct account using **az login**
* You are using the correct subscription in case you have more than one
* You specify all required parameters for the command you are using. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest) for required parameters and valid values.