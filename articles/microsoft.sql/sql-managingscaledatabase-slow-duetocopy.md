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
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
You have initiated an scale operation on your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->**. 

The change of performance tier operation takes a variable amount of time depending on the mechanism used for the change. In some cases, the change can be done without copying data, and it is then very quick - less than 1 minute. In others, unfortunately, it requires a copy, which proportional to the database size. Please refer links below, which document the maximum expected duration as 6 hours for Standard tier operations, which is how long a copy of the largest allowed database size on the smallest / least performant performance tier would take. We are working on several improvements introducing a pause/resume capability which takes less than 1 minute in all cases, as well as improvements so that a copy is not required. 

## **Recommended documents**
[Azure SQL database DTU resource limits](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits/)<br>
