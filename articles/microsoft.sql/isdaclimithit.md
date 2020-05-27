<properties
	pageTitle="DAC access limit reached"
	description="Dedicated Admin Connection Limit reached"
	infoBubbleText="Found DAC access limit issue"
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy, VMMicrosoft"
	ms.author="subbuk, vimahadi"
	displayOrder=""
	articleId="IsDACLimitHit_305D2B89-1F46-4FD7-B654-1F51C08F26C1"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980414,3260429"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC, the database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->, DAC (Dedicated Admin Connection) limit of one was reached and therefore new connection(s) were denied.

Dedicated Admin connection (DAC) for administrators are solely for diagnosing under rare circumstances and with limitations. To guarantee that there are resources available for the connection, only one DAC is allowed at a time. In your case, DAC connection was already active, and the new request to connect your database through the DAC was denied with error.

<!--/issueDescription-->

## **Recommended Documents**

* [Dedicated Administrator Access Limitations](https://docs.microsoft.com/sql/database-engine/configure-windows/diagnostic-connection-for-database-administrators?view=sql-server-2017#restrictions)
