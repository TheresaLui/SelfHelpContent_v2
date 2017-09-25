<properties
	pageTitle="Database Connectivity issue due to driver detected"
	description="IsTediousDriverRedirected"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="aamalvea"
	displayOrder=""
	articleId="IsTediousDriverRedirected_3946B48A-B9F4-4A20-9AA3-5BEE3E1FCFED"
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


