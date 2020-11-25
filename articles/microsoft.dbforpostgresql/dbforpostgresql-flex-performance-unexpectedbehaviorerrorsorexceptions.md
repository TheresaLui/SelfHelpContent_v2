<properties
    pageTitle="Troubleshoot query execution problems in Azure Database for PostgreSQL"
    description="Troubleshoot query execution problems in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="110"
    selfHelpType="generic"
    supportTopicIds="32640026, 32781014"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-performance-unexpectedbehaviorerrorsorexceptions"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshoot query execution problems in Azure Database for PostgreSQL

Query execution problems can be caused by the database engine itself or by the interaction of the database engine and the service. Follow the recommended steps to troubleshoot your problem.

## **Recommended Steps**

* Review your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.

