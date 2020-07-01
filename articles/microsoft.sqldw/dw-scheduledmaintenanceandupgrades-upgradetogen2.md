<properties
    pageTitle="Upgrading to Gen2"
    description="Upgrading to Gen2"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635200"
    productPesIds="15818"
    displayOrder="51"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-scheduledmaintenanceandupgrades-upgradetogen2"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Upgrading to Gen2

## **Recommended Steps**

* See if the lower compute tiers (DWUc400 and less) are [available in your region](https://docs.microsoft.com/azure/sql-data-warehouse/gen2-migration-schedule?branch=pr-en-us-66148#automated-schedule-and-region-availability-table)
* You may experience a period of degradation in performance while the upgrade process continues to upgrade the data files in the background. The total time for the performance degradation will vary dependent on the size of your data files.
* To expedite the background data migration process, you can immediately force data movement by running [Alter Index rebuild](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-index) on all primary columnstore tables you'd be querying at a larger SLO and resource class
* The actual downtime for the upgrade is only the time it takes to pause and resume the service, which is between 5 to 10 minutes. After the brief down-time, a background process will run a storage migration. The length of time for the background process is dependent on the size of your data warehouse.
  
## **Recommended Documents**

* [Upgrade to Gen2](https://docs.microsoft.com/azure/sql-data-warehouse/upgrade-to-latest-generation)
