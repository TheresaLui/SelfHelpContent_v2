<properties
    pageTitle="Creating and managing databases in Azure Database for PostgreSQL"  
    description="Creating and managing databases in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
	authors="Xin-Cheng"
	ms.author="chengxin"
    displayOrder="540"
    selfHelpType="generic"
    supportTopicIds="32684527"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-create-databases"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Creating and managing databases in Azure Database for PostgreSQL

Databases in Azure Database for PostgreSQL servers can be managed through the ARM template, using the Azure CLI and by calling our REST APIs. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Charset and collation are the only database properties that are supported in current framework. Please refer to [Supported charset and collation](https://www.postgresql.org/docs/current/collation.html) for more information. If you would like to change other properties during database creation or update, connect to Postgres using a client like Azure CLI and execute [CREATE DATABASE](https://www.postgresql.org/docs/current/sql-createdatabase.html) or [ALTER DATABASE](https://www.postgresql.org/docs/current/sql-alterdatabase.html).
* Please note: "Update databases" is not an available option in the ARM Template. Please make sure charset and collation for a database stay the same when you rerun the deployment.
        
* If you are using Azure CLI:

    * Make sure you are signed-in to the correct account using az login
    * Ensure you are using the correct subscription, in case you have more than one
    * Specify all required parameters in az postgres with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest) for required parameters and valid values.

* Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/) for guidance on using the REST API.
