<properties
	pageTitle="Database connectivity - Long Login issue"
	description="LongLogin"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	authorAlias="subbuk"
	displayOrder=""
	articleId="IsLongLogin_56EB94E0-398D-4557-A743-4918A95B7EA9"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980402"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that logging to <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> is taking longer than the usual time.

This typically means that logins are taking longer than 14 seconds. The most likely cause is either SQL server is having issues with performance, xdbhost is having issues in duplicating the socket to SQL, or both.
<!--/issueDescription-->

## **Recommended Documents**
* [Azure SQL Database Connectivity Architecture](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture)
* [This article](https://docs.microsoft.com/azure/sql-database/sql-database-develop-direct-route-ports-adonet-v12)  discusses the port ranges for connections inside and outside of Azure due to the connection policy   
