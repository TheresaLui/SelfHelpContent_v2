<properties
    pageTitle="Error while scaling a resource in Azure Database for PostgreSQL"
    description="Error while scaling a resource in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32780924"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-scaling-errorsscalingaresource"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Error while scaling a resource in Azure Database for PostgreSQL

## **Recommended Steps**

* Connections are dropped and no new connections can be established while compute is scaled:

    * Compute scaling requires a server restart. We recommend that you implement retry logic so that your application can seamlessly reconnect to the Postgres server after the scale operation is completed. Storage scaling does not cause a restart.

* Scaling fails with the error message, "Service is temporarily busy and the operation cannot be performed. Please try again later":

    * Try to scale the server again, after several minutes have passed

