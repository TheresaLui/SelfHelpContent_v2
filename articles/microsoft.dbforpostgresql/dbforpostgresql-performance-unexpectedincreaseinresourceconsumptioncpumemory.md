<properties
    pageTitle="Troubleshooting unexpected increase in resource consumption"
    description="Troubleshooting unexpected increase in resource consumption"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="100"
    selfHelpType="generic"
    supportTopicIds="32640027"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="64dc203f-500c-43b0-9096-2114c4910381"
/>

# Troubleshooting unexpected increase in resource consumption

Increase in resource consumption can be a result of an explicit user action or changes in the workload.

## **Recommended Steps**

* Ensure there are no changes to the pricing tier of your service that might have triggered it
* Adjust the pricing tier commensurate to the increase in the workload
* Check if there are any schema changes, for example whethere an index was dropped
* Ensure that the table statistics are up to date

## **Recommended Documents**

* [Performance Recommendations in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)
