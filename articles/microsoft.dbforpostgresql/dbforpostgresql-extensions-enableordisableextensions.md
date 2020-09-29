<properties
    pageTitle="Enable extensions"
    description="How to enable extensions"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="510"
    selfHelpType="generic"
    supportTopicIds="32639975"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="61c08d2a-d2e9-4163-bd62-18f200c9ed42"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Enabling PostgreSQL extensions

## **Recommended steps**

Most extensions can be enabled using the SQL command `CREATE EXTENSION <Extension name>;`

Some extensions may have different instructions around enabling or disabling them. We recommend that you review your specific extension's documentation to learn more. The [Azure Database for PostgreSQL extensions document](https://docs.microsoft.com/azure/postgresql/concepts-extensions) provides links to each extension's documentation. [This document](https://docs.microsoft.com/azure/postgresql/concepts-extensions) also provides additional guidance for some extensions, for example how to set-up TimescaleDB in Azure Database for PostgreSQL.
