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

# We found automatic indexing recommendations for your database.

<!--issueDescription-->
Our internal service telemetry detected automatic tuning recommendation(s) in the database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on the server **<!--$ServerName-->ServerName<!--/$ServerName-->**. Creating the recommended indexes or modifying existing indexes may improve database performance. 
<!--/issueDescription-->

## **Recommended Steps**

Apply the index recommendations for potential performance improvements:  
1. Go to Azure portal > All services > SQL databases  
2. Select database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->**  
3. Click on Performance Recommendations  
4. Find the table titled "Recommendations," which shows actions that you can apply to optimize the performance of your database  
5. Start with the actions labeled "HIGH IMPACT" and consider performing the action recommended  
    a. Note that creating indexes on large tables can take a significant amount of time and resources. We recommend only creating indexes when your database is under non-peak loads.
6. Continue to work your way through the medium and low impact recommendations in order

Depending on the estimated performance gain, recommendations are categorized as high, medium, or low. Adding new indexes will increase storage usage and can impact data modification performance.  
  
See the referenced articles for more details.

## **Recommended Documents**

* [Find and Apply Performance Recommendations](https://docs.microsoft.com/en-us/azure/azure-sql/database/database-advisor-find-recommendations-portal)
* [Performance Recommendations for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-advisor)
* [Automatic Index Management in Azure SQL database](https://docs.microsoft.com/archive/blogs/sqlserverstorageengine/automatic-index-management-in-azure-sql-db)
