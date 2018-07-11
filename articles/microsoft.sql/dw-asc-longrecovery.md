<properties 
    pageTitle="Long running database recovery detected" 
    description="Long recovery" 
    infoBubbleText="Long running database recovery detected. See details for more info." 
    service="microsoft.sql" 
    resource="" 
    authors="saltug" 
    displayOrder="" 
    articleId="LongRecovery-13FA01C0-7B1F-4F2B-ADAA-3792A581BF40" 
    diagnosticScenario="" 
    selfHelpType="rca" 
    supportTopicIds="" 
    resourceTags="datawarehouse" 
    productPesIds="" 
    cloudEnvironments="public" 
/> 
# We ran diagnostics on your resource and found an issue 

<!--issueDescription--> 
We have detected that your SQL Data Warehouse instance (server **<!--$ServerName--> ServerName <!--/$ServerName-->** , database **<!--$DatabaseName--> DatabaseName <!--/$DatabaseName-->**) is unavailable due to a long running transaction rollback. Long running recovery is caused when a large transaction's query is cancelled either by the user, by a query failure, or by a pause or scale operation. When the database comes online after the issue the transaction needs to be rolled back before the database becomes available, causing a longer than normal amount of time needed to resume the SQL Data Warehouse.
<!--/issueDescription--> 

We estimate the rollback should complete in **<!--$RecoveryEstimate--> RecoveryEstimate <!--/$RecoveryEstimate-->** hours from now, and your instance will be available again. 

If desired, we can restore a parallel instance from a backup taken prior to the large transaction. You can use this second instance in a temporary manner, or rollback your workload and permanently use it. Please restore documentation for the required steps:

> [Restore Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-database-portal)

One of the ways to avoid this in the future is to ensure that there are no long running transactions before you start a scale operation. Also, we suggest you to review transaction optimization guidance to minimize logging and thus avoid long running recovery: 

> [Optimizing transactions in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-develop-best-practices-transactions) 