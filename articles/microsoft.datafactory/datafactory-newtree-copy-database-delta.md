<properties
	pageTitle="Delta Load from Relational Database"
	description="Only copy new or modified records"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="4bc42034-2ae1-404a-bce9-149311352392"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629458, 32629459"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public"
/>

# Incremental Copy from Database

## **Recommended Steps**

* Delta data loading using watermark: <br>

  * Define a watermark column in source database, a column that has the last updated time stamp or an incrementing key
  * Delta loading solution loads changed data between an old watermark and a new one

* Delta data loading using _Change Tracking_: <br>

  * Available when loading from data stores such as _SQL Server_ and _Azure SQL Database_
  * Need to enable _Change Tracking_ in source database

## **Recommended Documents**

* Incremental loading from one table: <br>
  * [ADF Portal](https://docs.microsoft.com/azure/data-factory/tutorial-incremental-copy-portal) <br>
  * [PowerShell](https://docs.microsoft.com/azure/data-factory/tutorial-incremental-copy-powershell) <br>
* Incremental loading from multiple tables: <br>
  * [ADF Portal](https://docs.microsoft.com/azure/data-factory/tutorial-incremental-copy-multiple-tables-portal) <br>
  * [PowerShell](https://docs.microsoft.com/azure/data-factory/tutorial-incremental-copy-multiple-tables-powershell) <br>
* Use _Change Tracking_ technology: <br>
  * [ADF Portal](https://docs.microsoft.com/azure/data-factory/tutorial-incremental-copy-change-tracking-feature-portal) <br>
  * [PowerShell](https://docs.microsoft.com/azure/data-factory/tutorial-incremental-copy-change-tracking-feature-powershell) <br>
