<properties
	pageTitle="Scale database - slow due to copy"
	description="Performance tier change is slow due to copy"
	infoBubbleText="Found an ongoing scale issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="Anvesha4,Johirsch"
	ms.author="Johirsch"
	displayOrder="15"
	articleId="UpdaSloCopying_A5D06371-7DA1-4999-B474-9B020FEB9071"
	diagnosticScenario="SqlProvision"
	selfHelpType="Diagnostics"
	supportTopicIds="32630431,32630452,32574333"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>
# We ran diagnostics on your resource and found an ongoing scale issue
<!--issueDescription-->
You have initiated a scale operation on your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->**. This operation is delayed due to slow copy of data between source and target performance tiers. The time required to complete an operation to change the performance tier of an Azure SQL Database depends on the mechanism used for the change.
<!--/issueDescription-->

### **Root Cause Investigation**

The time required to complete an operation to change the performance tier of an Azure SQL Database depends on the mechanism used for the change. In some cases, the change can be done in as little as five minutes without copying data. In other cases, unfortunately, it requires a copy, which may take longer depending on the size of the database. For guidance on how long your scaling operation should take under normal circumstances, use the following links:

* [Scaling a single database](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale#change-compute-resources-vcores-or-dtus)<br>
* [Scaling an elastic pool](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale#change-compute-resources-vcores-or-dtus)<br>

We are working on several improvements including: <br>

* reducing how often a copy is required, and
* introducing pause/resume capability which can be used instead of scaling, and is expected to take less than 5 minutes in all cases. For more information, please refer to the links below.

## **Recommended Documents**

* [Azure SQL scale single DB resources](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale)<br>
* [Azure SQL scale elastic pool resources](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale)<br>
* [Azure SQL database DTU-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits/)<br>
* [Azure SQL database vCore-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases/)
