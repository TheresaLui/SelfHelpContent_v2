<properties
    pageTitle="The session limit for the database has been reached"
    description="Diagnose and resolve issues connecting to Azure SQL Database"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745427"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="CD72434D-E71D-4D81-800B-7AF0A6B97CEC"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# The session limit for the database has been reached

For DTU-based service tiers, SQL Database limits the number of [concurrent sessions](https://docs.microsoft.com/azure/azure-sql/database/resource-limits-dtu-single-databases?WT.mc_id=pid:13491:sid:32745427) allowed to the database.  Your application is attempting to open more connections than is allowed for your service tier, which is usually due to increased workload.  If your application uses connection pooling, a slowdown in query response time may cause a constant rate of frontend requests to require more backend database connections.

**NOTE**: This error number is used when hitting the limit on either sessions (i.e., connections) or requests (i.e., concurrent queries). Confirm that your error message indicates you are hitting the *session limit*.

## **Recommended Steps**

For an immediate solution, scale your database to a larger DTU-based service tier sufficient to handle the workload.  For a longer-term solution, you should either:
-  Use [Query Performance Insight](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance?WT.mc_id=pid:13491:sid:32745427) to identify poorly performing or resource intensive queries that need tuning, so that your workload can be handled by the current service tier, or
- Switch to an elastic pool or vCore-based purchasing models, which effectively removes the session limit (setting it to 30000)


## **Recommended Documents**

* [Resource limits for single databases using the vCore purchasing model](https://docs.microsoft.com/azure/azure-sql/database/resource-limits-vcore-single-databases?WT.mc_id=pid:13491:sid:32745427)
