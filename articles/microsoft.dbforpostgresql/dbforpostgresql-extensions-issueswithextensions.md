<properties
    pageTitle="Issues with extensions"
    description="Guidance on what to do if you encounter an issue with a Postgres extension"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="520"
    selfHelpType="generic"
    supportTopicIds="32639990"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="bd1b1e10-24c2-4900-a99f-98c4f1295e4b"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with PostgreSQL extensions

## **Recommended steps**

We recommend that you review your specific extension's documentation to learn more. The [Azure Database for PostgreSQL extensions document](https://docs.microsoft.com/azure/postgresql/concepts-extensions) provides links to each extension's documentation. [This document](https://docs.microsoft.com/azure/postgresql/concepts-extensions) also provides additional guidance for some extensions like postgres_fdw and TimescaleDB in Azure Database for PostgreSQL.

You can check an extension's version by querying the following on your server and checking the default_version column.
`SELECT * FROM pg_available_extensions;`
