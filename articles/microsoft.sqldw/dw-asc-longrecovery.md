<properties 
    pageTitle="Long running database recovery detected" 
    description="Long recovery" 
    infoBubbleText="Long running database recovery detected. See details for more info." 
    service="microsoft.sql" 
    resource="" 
    authors="saltug" 
    ms.author="saltug"
    displayOrder="" 
    articleId="LongRecovery-13FA01C0-7B1F-4F2B-ADAA-3792A581BF40" 
    diagnosticScenario="dwasc" 
    selfHelpType="rca" 
    supportTopicIds="" 
    resourceTags="datawarehouse" 
    productPesIds="" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
	ownershipId="AzureData_AzureSQLDB"
/> 
# We ran diagnostics on your resource and found an issue 

<!--issueDescription--> 
We have detected that your SQL Data Warehouse instance (server **<!--$ServerName--> ServerName <!--/$ServerName-->** , database **<!--$DatabaseName--> DatabaseName <!--/$DatabaseName-->**) is/was unavailable due to a long running transaction rollback. Long running recovery is caused when a large transaction's query is cancelled either by the user, by a query failure, or by a pause or scale operation. When the database comes online after the issue the transaction needs to be rolled back before the database becomes available, causing a longer than normal amount of time needed to resume the SQL Data Warehouse.
<!--/issueDescription--> 

#### **Recommended Documents**

* To prevent this scenario from occurring again, we recommend allowing existing transactions to finish before you initiate a pause or scale operation: [Pausing and resuming compute](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-compute-overview#pausing-and-resuming-compute)
* Optimizing your transactions will also help to minimize logging and avoid long running recovery: [Optimizing transactions in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-develop-best-practices-transactions) 
