<properties
	pageTitle="Database Connectivity issue due to driver detected"
	description="IsCustomerBypassingGW"
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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
 We’ve detected a possible issue with your driver’s implementation of TDS routing protocol. This could be leading it to look for the database in an old location. In the immediate, bypassing redirection by forcing your connection policy to Proxy will restore your connectivity. In the future, please consider upgrading your driver to prevent these issues.
<!--/issueDescription-->

For more information about redirection, see [Connect to Azure SQL Database V12 via Redirection](https://blogs.msdn.microsoft.com/sqlcat/2016/09/08/connect-to-azure-sql-database-v12-via-redirection/)

