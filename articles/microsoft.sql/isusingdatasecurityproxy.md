<properties
	pageTitle="Database Connectivity issue due to invalid credentials detected"
	description="Database Connectivity issue due to invalid credentials using Data Security Proxy"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy, swbhartims"
  	ms.author="subbuk, swbharti"
	displayOrder=""
	articleId="IsUsingDataSecurityProxy_20566AB1-A1DE-46DD-9A10-D875D54E326F"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public" 
/>
# Database Connectivity issue due to invalid credentials using Data Security Proxy

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We notice secured connection string(s) were used for connecting to your <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->. Secured connection strings <i> <!--$ServerName-->ServerName<!--/$ServerName-->.database.secure.windows.net </i> is used for down level clients connecting to security enabled database using Table Auditing.
Table Auditing feature is now deprecated and we highly recommend you to switch to Blob Auditing, which does not require to use down-level client connection string (<i><!--$ServerName-->ServerName<!--/$ServerName-->.database.secure.windows.net </i>) to connect to your database.
<!--/issueDescription-->

## **Recommended Documents**

* [Blob Storage Auditing](https://docs.microsoft.com/azure/sql-database/sql-database-auditing)
* [Table Auditing (Deprecated feature)](https://docs.microsoft.com/azure/sql-database/sql-database-auditing-and-dynamic-data-masking-downlevel-clients)

