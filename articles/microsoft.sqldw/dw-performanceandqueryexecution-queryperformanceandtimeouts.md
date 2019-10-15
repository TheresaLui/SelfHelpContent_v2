<properties
    pageTitle="Query performance and timeouts"
    description="Query performance and timeouts"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635214"
    productPesIds="15818"
    displayOrder="32"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-performanceandqueryexecution-queryperformanceandtimeouts.md"
    cloudEnvironments="public"
/>

# Query performance and timeouts

## **Recommended Steps**

* If you experience slow query or load performance, ensure you have allocated enough memory. Refer to the following documentation for [guidance](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management#example-code-for-finding-the-best-resource-class) around resource classes and selecting the appropriate one.
* You can also check to see which resources a request is waiting for by visiting the following [documentation](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload)
* Internal DMS errors related to columnstore compression exceeding the remaining memory can be addressed by [increasing the resource class](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class)

## **Recommended Documents**

* [Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)
