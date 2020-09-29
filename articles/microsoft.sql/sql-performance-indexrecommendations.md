<properties
    pageTitle="Automatic Tuning Recommendation(s) Detected"
    description="performance/automatic tuning recommendation(s) detected"
    infoBubbleText="Found automatic tuning recommendation(s) on this database. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="whatstartwo"
    ms.author="xinyl"
    displayOrder=""
    articleId="IndexRecommendation_EF325930-F464-45F2-AFEF-E2897BC26951"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32630434,32630450,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public,MoonCake,fairfax,usnat,ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# We ran diagnostics on your resource and found automatic tuning recommendation(s).

<!--issueDescription-->
Our internal service telemetry detected automatic tuning recommendation(s) in the database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on the server **<!--$ServerName-->ServerName<!--/$ServerName-->** between **<!--$StartTime-->StartTime<!--/$StartTime--> UTC** and **<!--$EndTime-->EndTime<!--/$EndTime--> UTC**. Creating these indexes may improve performance for the queries that triggered the missing index recommendation(s). Adding new indexes will increase storage requirements and potentially impact data modification performance.
<!--/issueDescription-->

## **Recommended Steps**

Depending on the estimated performance gain, recommendations are categorized as high, medium, or low. Consider creating recommended index(es) in the order of their impact (high, medium, low). To apply the recommendation(s), go to Azure portal > All services > SQL databases > Performance recommendations. Note that creating indexes on the table with a large number of rows may take significant amount of time and resources. Please plan ahead and avoid creating indexes during time periods with a high concurrent workload. See the referenced article for more details.

## **Recommended Documents**

* [Performance recommendations for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-advisor)
* [Automatic index management in Azure SQL database](https://docs.microsoft.com/archive/blogs/sqlserverstorageengine/automatic-index-management-in-azure-sql-db)
