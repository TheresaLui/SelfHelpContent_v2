<properties
	pageTitle="Database connectivity - Downtime due to Long Recovery"
	description="Long Recovery"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy, VMMicrosoft"
	ms.author="subbuk, vimahadi"
	displayOrder=""
	articleId="IsLongRecovery_DB131178-E313-4877-AF3E-8EA46B7D642C"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> was going through a long recovery operation at this time. Recovery operation is a database process that occurs when a database first restarts after a downtime due to user initiated or system side operation. This rolls back all your in-flight but uncommitted transactions at the time of restart, and during this time the database becomes unavailable. Depending on the size of transactions to rollback, this activity takes time proportional to the size of the active transactions. Once this recovery operation is complete, your database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> should become available. As of <!--$TimeOfExecution-->TimeOfExecution<!--/$TimeOfExecution-->, the estimated time of total recovery is <!--$TotalTime-->TotalTime<!--/$TotalTime-->.
<!--/issueDescription-->
