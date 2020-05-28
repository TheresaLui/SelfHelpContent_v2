<properties
    pageTitle="Troubleshooting unexpected increase in resource consumption"
    description="Troubleshooting unexpected increase in resource consumption"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="100"
    selfHelpType="generic"
    supportTopicIds="32640158"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="58c3084a-4d18-44c2-8a21-e27d51c2f130"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Troubleshooting unexpected increase in resource consumption

Increase in resource consumption can be a result of an explicit user action or changes in the workload.

## **Recommended Steps**

* Ensure there are no changes to the pricing-tier of your service that might have triggered it
* Adjust the pricing-tier commensurate to the increase in the workload
* Check if there are any schema changes, for example was an index dropped
* Ensure that the statistics are up to date

## **Recommended Documents**

* [Performance Recommendations in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-performance-recommendations)<br>
* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)
