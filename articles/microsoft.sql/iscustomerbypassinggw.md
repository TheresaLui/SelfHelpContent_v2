<properties
	pageTitle="Database Connectivity issue due to driver detected"
	description="Database Connectivity issue due to driver detected"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="aamalvea"
	displayOrder=""
	articleId="IsCustomerBypassingGW_6219D2CD-8D65-4F26-962D-B47F5B77F759"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    ms.author="aamalvea"
	ownershipId="AzureData_AzureSQLDB"
/>

# Database Connectivity issue due to driver detected

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We’ve detected a possible issue with your driver’s implementation of TDS routing protocol. This could be leading it to look for the database in an old location. Bypassing redirection by forcing your connection policy to Proxy will restore your connectivity. In the future, please consider upgrading your driver to prevent these issues.
<!--/issueDescription-->

For more information about redirection, see [Azure SQL Connectivity Architecture](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture).

