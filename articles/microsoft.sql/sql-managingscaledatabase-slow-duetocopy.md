<properties
	pageTitle="Scale database - slow due to copy"
	description="Performance tier change is slow due to copy"
	infoBubbleText="Found an ongoing scale issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="Anvesha4"
	displayOrder="15"
	articleId="UpdaSloCopying_A5D06371-7DA1-4999-B474-9B020FEB9071"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32574333"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an ongoing scale issue.

**Summary of issue**<br>
You have initiated an scale operation on your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->**. <br>
This operation is proceeding slowly due to slow copy. 

**Root cause investigation**<br>
The change of performance tier operation takes variable amount of time depending on the mechanism used for the change. In some cases, the change can be done without copying data, which is very quick - takes less than 5 minutes. In others, unfortunately, it requires a copy, which proportional to the database size. Please refer links below, which document the maximum expected duration as 6 hours for Standard tier  operations, which is how long a copy of the largest allowed database size on the smallest / least performant performance tier would take. For scale-up operations within Premium tiers, you can expect copying to last upto 3 hours. We are working on several improvements including a) reducing how often copy is required, and b) introducing pause/resume capability which can be used instead of scale, and is expected to take less than 5 minutes in all cases.

## **Recommended documents**
[Azure SQL scale single DB resources](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale)<br>
[Azure SQL scale elastic pool resources](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale)<br>
[Azure SQL database DTU-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits/)<br>
[Azure SQL database vCore-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases/)<br>
