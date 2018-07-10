<properties
	pageTitle="Scale database - slow due to workload"
	description="Performance tier change is slow due to workload"
	infoBubbleText="Found an ongoing scale issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="Anvesha4"
	displayOrder="16"
	articleId="UpdaSloKillLongRunningTransactions_A5D06371-7DA1-4999-B474-9B020FEB9071"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32574333"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
You have initiated an scale operation on your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->**. 

This operation is proceeding very slowly. Slow copy can be due to various factors, like database size or database having too high CPU/IO. The scale process is implemented as a copy between instances with different resource allocations, and that copy depends on CPU and IO resources on the source database. If the database is under high resource utilization from user workload, then the copy proceeds very slowly. The copy is designed to not interfere with user workload and thus throttles its rate in this situation. The scale operation will proceed more rapidly if the user workload is reduced. We are working on improvements to be able to scale up/down a database in a short (minutes) and constant time regardless of workload.

## **Recommended steps**
Please reduce the workload on your database to reduce throttling of the scale operation. </br>

## **Recommended documents**
[Azure SQL database DTU resource limits](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits/)<br>
