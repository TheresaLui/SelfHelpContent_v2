<properties
	pageTitle="Scale database - slow due to workload"
	description="Performance tier change is slow due to workload"
	infoBubbleText="Found an ongoing scale issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="Anvesha4,andikshi"
	ms.author="ansinh,andikshi"
	displayOrder="17"
	articleId="UpdateSloSlowDuetoWorkload_3208A0BE-EA03-4A0E-B7C9-0A2219299B4F"
	diagnosticScenario="DiagnosticId.SqlProvision"
	selfHelpType="Diagnostics"
	supportTopicIds="32574333"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>
# We ran diagnostics on your resource and found an ongoing scale issue

<!--issueDescription-->
You have initiated a scale operation on your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->**. This operation is proceeding slowly due to user workload on the database.
<!--/issueDescription-->

### Root Cause Investigation

The scale operation is implemented as a copy of data between instances with different resource allocations, and it can depend on factors like database size and CPU/IO resources on the source database. The copy operation is designed to not interfere with user workload, and therefore is significantly throttled when there is user workload on the database. If the database is under high resource utilization from user workloads, then the copy operation proceeds very slowly. The scale operation will proceed more rapidly if the user workload is reduced. We are working on improvements to be able to scale up/down a database in a short time (minutes) and constant time, regardless of workload.

## **Recommended Steps**

* Reduce the workload on your database to reduce throttling of the scale operation

## **Recommended Documents**

* [Use Query performance insights to identify the queries which are causing the high CPU/IO consumption](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance)
* [Enabling Automatic tuning provides peak performance and stable workloads through continuous performance tuning by utilizing Artificial Intelligence](https://docs.microsoft.com/azure/sql-database/sql-database-automatic-tuning)
* [Azure SQL database DTU-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits/)
* [Azure SQL database vCore-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases/)
* [Azure SQL scale single DB resources](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale)
* [Azure SQL scale elastic pool resources](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale)
