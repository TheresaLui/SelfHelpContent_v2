<properties
    pageTitle="Troubleshooting unexpected increase in resource consumption"
    description="Troubleshooting unexpected increase in resource consumption"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="100"
    selfHelpType="generic"
    supportTopicIds="32781015"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-performance-unexpectedincreaseinresourceconsumptioncpumemory"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting unexpected increase in resource consumption

Increase in resource consumption can be a result of an explicit user action or changes in the workload. Sometimes increased CPU usage is also caused by an issue with PostgreSQL internal processes, such as autovacuum not running as expected.

## **Recommended Steps**

* Ensure that there are no changes to the pricing tier of your service that might have triggered the increase
* Adjust the pricing tier commensurate to the increase in the workload
* Check if there are any schema changes, for example, whether an index was dropped
* Ensure that the table statistics are up-to-date
* Review when your tables were last vacuumed and tune the threshold parameters 

