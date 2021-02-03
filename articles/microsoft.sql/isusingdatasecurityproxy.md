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
	diagnosticScenario="SqlConnectivity"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>
# Database connectivity issue due to auditing enabled secured connections

<!--issueDescription-->
We noticed that you are connecting to an auditing-enabled database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> using secured connection strings (<!--$ServerName-->ServerName<!--/$ServerName-->.database.secure.windows.net).
<!--/issueDescription-->

The secured connection strings were only used for databases with Table Auditing enabled, which is now deprecated. Connecting to database using the secure endpoints is unsupported, may cause connection errors/issues, and it is not a recommended option. We highly recommend you to use blob auditing which does not require any changes to your connection strings, and it is more efficient and less error prone.

## **Recommended Documents**

* [Blob Storage Auditing](https://docs.microsoft.com/azure/sql-database/sql-database-auditing)
