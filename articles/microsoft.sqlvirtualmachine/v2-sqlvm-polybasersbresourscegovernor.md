<properties
  pagetitle="Polybase&#xD;"
  description="Polybase, R Services, Service Broker, Resource governor"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740088"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="c47f08aa-e28b-4b91-b0a4-35c11bddabd1"
  ownershipid="AzureData_AzureSQLVM" />
# Polybase

Most users can resolve issues concerning SQL PolyBase by using the following steps. 

## **Recommended Steps** 

* **Set up PolyBase** 

   * [Install Polybase](https://docs.microsoft.com/sql/relational-databases/polybase/polybase-installation?view=sql-server-ver15) 

   * [Configure Polybase](https://docs.microsoft.com/sql/relational-databases/polybase/polybase-configure-sql-server?view=sql-server-ver15). To use PolyBase, you must have **sysadmin or CONTROL SERVER** level permissions on the database. 

   * To **change the service accounts** for the PolyBase Engine and PolyBase Data Movement service, uninstall and reinstall the PolyBase feature. To understand restrictions with PolyBase, see [features and limitations](https://docs.microsoft.com/sql/relational-databases/polybase/polybase-versioned-feature-summary?view=sql-server-ver15#known-limitations). 

   * Setting up PolyBase with Azure data lake Gen2 as external source is [not supported](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) as PolyBase doesn't support **ABFS API**. See additional [PolyBase limitations](https://docs.microsoft.com/sql/relational-databases/polybase/polybase-versioned-feature-summary?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support).


* **Configuring Resource Governor** 

   You can configure Resource Governor to [limit CPU usage by backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/use-resource-governor-to-limit-cpu-usage-by-backup-compression-transact-sql?view=sql-server-ver15).

## **Recommended Documents** 

* [Enable SQL Server to execute external scripts using Polybase](https://docs.microsoft.com/sql/machine-learning/install/sql-machine-learning-services-windows-install?view=sql-server-ver15#enable-script-execution) 
* [Create an external data source for querying using SQL Server](https://docs.microsoft.com/sql/t-sql/statements/create-external-data-source-transact-sql?view=sql-server-ver15&tabs=dedicated) 
* [Configure Resource Governor using a template](https://docs.microsoft.com/sql/relational-databases/resource-governor/configure-resource-governor-using-a-template?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)