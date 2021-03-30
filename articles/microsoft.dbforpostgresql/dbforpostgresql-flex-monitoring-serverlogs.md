<properties
    pageTitle="Monitoring server logs"
    description="Monitoring server logs"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="270"
    selfHelpType="generic"
    supportTopicIds="32780882"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-monitoring-serverlogs"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Monitoring server logs

Azure Database for PostgreSQL has error, query, and audit logs available. Query and error logs can be used to identify, troubleshoot, and repair configuration errors and sub-optimal performance. 

Visit the support topic Security >> Auditing for guidance on audit logs.


## **Recommended Steps**

* Logs can be consumed through Azure diagnostic logging (which routes to storage account, Event Hub, or Azure Monitor logs).
* Familiarize yourself with the [PostgreSQL log parameters](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/how-to-configure-postgres-log-settings/ba-p/1214716)
* Verbose logging will cause a significant performance overhead. We recommend that you only use statement logging parameters such as `log_statement` and `log_min_duration_statement` for short periods of troubleshooting. 
* Access to transaction logs is not available
* The .log file format is not available for flexible server

