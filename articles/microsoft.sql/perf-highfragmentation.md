<properties 
    pageTitle="High unused space detected" 
    description="High unused space" 
    infoBubbleText="High unused space detected. See details for more info." 
    service="microsoft.sql" 
    resource="" 
    authors="zhimwang" 
    displayOrder="" 
    articleId="HighFrag-522DA2B1-73AD-4EA2-AD1C-5C4FDEB97F35"
    diagnosticScenario="" 
    selfHelpType="rca" 
    supportTopicIds="" 
    resourceTags="" 
    productPesIds="" 
    cloudEnvironments="public" 
/> 
# We ran diagnostics on your resource and found an issue 

<!--issueDescription--> 
Your pool has more than 100GB of disused storage space.  File space allocated is not automatically reclaimed when data is deleted. If this space will be used soon, disregard this insight.
<!--/issueDescription--> 

#### **Recommended documents**

If this space is no longer needed, you can reclaim it by following suggestions detailed in the [Manage file space in Azure SQL Database](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-file-space-management) in the Reclaim unused allocated space section.