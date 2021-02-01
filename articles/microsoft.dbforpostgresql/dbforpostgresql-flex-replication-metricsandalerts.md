<properties
    pageTitle="Monitoring replication in Azure Database for PostgreSQL"
    description="Metric issues"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="430"
    selfHelpType="generic"
    supportTopicIds="32780915"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-replication-metricsandalerts"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Monitoring replication

## **Recommended Steps**

* `SELECT * FROM pg_replication_slots;`
   
   PostgreSQL provides the [pg_replication_slots](https://www.postgresql.org/docs/current/view-pg-replication-slots.html) table for data on replication status. 
