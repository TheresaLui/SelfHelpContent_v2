<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for PostgreSQL server"
    description="Creating, scaling, and deleting an Azure Database for PostgreSQL server"
    service="microsoft.dbforpostgresql"
    resource="servers"
	authors="Xin-Cheng"
	ms.author="chengxin"
    displayOrder="540"
    selfHelpType="generic"
    supportTopicIds="32684527"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="44BF1BBE-80E0-40AC-AA31-ED9519FA3E82"
/>

# Creating, scaling, and deleting an Azure Database for PostgreSQL server

Databases in Azure Database for PostgreSQL servers can be managed through the ARM template, using the Azure CLI and by calling our REST APIs. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Charset and collation are the only database properties that are supported in current framework. Please refer to [Supported charset and collation](https://www.postgresql.org/docs/current/collation.html) for more information. If you would like to change other properties during database creation or update, connect to Postgres using a client like Azure CLI and execute [CREATE DATABASE](https://www.postgresql.org/docs/current/sql-createdatabase.html) or [ALTER DATABASE](https://www.postgresql.org/docs/current/sql-alterdatabase.html).
* To familiarize yourself with using ARM templates to create databases in Azure Database for PostgreSQL server, refer to [this sample template](https://github.com/Azure/azure-postgresql/tree/master/arm-templates)
* Please note: "Update databases" is not an available option in the ARM Template. Please make sure charset and collation for a database stay the same when you rerun the deployment.
        
* If you are using Azure CLI, review the [Single Server using Azure CLI](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-cli) and:

    * Make sure you are signed-in to the correct account using az login
    * Ensure you are using the correct subscription, in case you have more than one
    * Specify all required parameters in az postgres with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest) for required parameters and valid values.

* Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/) for guidance on using the REST API.

## **Recommended Documents**

* [Azure Database for PostgreSQL servers](https://docs.microsoft.com/azure/postgresql/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/postgresql/concepts-supported-versions)<br>
* [Compute and storage options](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)<br>
* [Limits](https://docs.microsoft.com/azure/postgresql/concepts-limits)
