<properties
    pageTitle="Automatic Indexing Recommendations Detected"
    description="SQL DB Performance: Automatic Indexing Recommendations Detected"
    infoBubbleText="We found automatic indexing recommendations for your database. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="ketho00"
    ms.author="ketho"
    displayOrder=""
    articleId="IndexRecommendation_EF325930-F464-45F2-AFEF-E2897BC26951"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32749514, 32749515, 32749517, 32749520"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public,MoonCake,fairfax,usnat,ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# We found automatic indexing recommendations for your database

<!--issueDescription-->
We detected automatic indexing recommendations on the database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on the server **<!--$ServerName-->ServerName<!--/$ServerName-->**. Creating the recommended indexes, or modifying existing indexes to reflect the create index recommendations, may improve database performance.
<!--/issueDescription-->

## **Recommended Steps**

To potentially improve your database performance, apply the index recommendations:
1. Go to Azure portal > All services > SQL databases  
2. Select database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->**  
3. Click on Performance Recommendations  
4. Find the table titled "Recommendations," which shows actions that you can apply to optimize the performance of your database  
5. Start with the actions labeled "HIGH IMPACT" and consider performing the action recommended  
    a. Note that creating indexes on large tables can take a significant amount of time and resources. We recommend only creating indexes when your database is under non-peak loads.  
    b. For more information on modifying existing indexes to reflect create index recommendations, see [SQL Server Index Design Guide](https://docs.microsoft.com/sql/relational-databases/sql-server-index-design-guide)
6. Continue to work your way through the medium and low impact recommendations in order

Depending on the estimated performance gain, recommendations are categorized as high, medium, or low. Adding new indexes will increase storage usage and can impact data modification performance.  
  
For more details, see the referenced articles below.

## **Recommended Documents**

* [Find and Apply Performance Recommendations](https://docs.microsoft.com/azure/azure-sql/database/database-advisor-find-recommendations-portal)
* [Performance Recommendations for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-advisor)
