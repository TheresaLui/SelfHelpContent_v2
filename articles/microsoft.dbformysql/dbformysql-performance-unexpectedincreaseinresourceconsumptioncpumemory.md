<properties
    pageTitle="Troubleshooting unexpected increase in resource consumption"
    description="Troubleshooting unexpected increase in resource consumption"
    service="microsoft.dbformysql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="100"
    selfHelpType="generic"
    supportTopicIds="32640096"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="64dc203f-500c-43b0-9096-2114c4910381"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting unexpected increase in resource consumption

Increase in resource consumption can be a result of an explicit user action or changes in the workload.

## **Recommended Steps**

* Ensure there are no changes to the pricing-tier of your service that might have triggered it
* Adjust the pricing-tier commensurate to the increase in the workload
* You can increase the IOPS available to your server by scaling up storage. IOPS scale with the size of the provisioned storage in a 3:1 ratio.
* Check if there are any schema changes, for example was an index dropped
* Ensure that the statistics are up to date

## **Recommended Documents**

* [Performance Recommendations in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)<br>
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
