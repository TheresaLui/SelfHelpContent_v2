<properties 
    pageTitle="High unused space detected" 
    description="High unused space" 
    infoBubbleText="High unused space detected. See details for more info." 
    service="microsoft.sql" 
    resource="" 
    authors="zhimwang" 
    displayOrder="" 
    articleId="HighFrag-522DA2B1-73AD-4EA2-AD1C-5C4FDEB97F35"
    diagnosticScenario="HighFragmentation" 
    selfHelpType="diagnostics" 
    supportTopicIds="31980401,32511226" 
    resourceTags="" 
    productPesIds="13491" 
    cloudEnvironments="public" 
/> 
# We ran diagnostics on your resource and found an issue 

<!--issueDescription--> 
We detected that your pool has more than 100GB of disused storage space in the past 30 minutes. This condition can occur when space used increases and data is subsequently deleted. File space allocated is not automatically reclaimed when data is deleted. 

Monitoring file space usage and shrinking data files may be necessary in the following scenarios:

* Allow data growth in an elastic pool when the file space allocated for its databases reaches the pool max size.
* Allow decreasing the max size of a single database or elastic pool.
* Allow changing a single database or elastic pool to a different service tier or performance tier with a lower max size.
<!--/issueDescription--> 

## **Recommended steps**

* If this space will be used soon, disregard this insight.
* If this space is no longer needed, you can reclaim it by following suggestions detailed in the [Manage file space in Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-file-space-management) in the Reclaim unused allocated space section.

## **Recommended Documents**
[Manage file space in Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-file-space-management)
