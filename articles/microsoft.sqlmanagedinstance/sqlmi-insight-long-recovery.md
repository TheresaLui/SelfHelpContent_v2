<properties
  	pageTitle="Managed Instance - Long recovery"
  	description="Managed Instance - Long recovery"
  	infoBubbleText="Database recovery is taking a long time."
  	service="microsoft.sql"
  	resource="managedInstances"
  	ms.author="v-anbozo"
  	authors="v-anbozo"
  	displayOrder=""
  	diagnosticScenario="SqlMIConnectivity_Long recovery"
  	selfHelpType="diagnostics"
  	supportTopicIds="32637216,32637254"
  	resourceTags=""
  	productPesIds="16259"
  	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  	articleId="sqlmanagedinstance-connectivity-long-recovery"
  	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Long recovery

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified database(s) <!--$affectedDatabases-->affectedDatabases<!--/$affectedDatabases--> on server <!--$ServerName-->ServerName<!--/$ServerName--> was going through a long recovery. They started at <!--$recoveryStarts-->recoveryStarts<!--/$recoveryStarts--> and lasted for <!--$recoveryDurations-->recoveryDurations<!--/$recoveryDurations-->. Recovery start time, recovery duration time  and name of the database in recovery are mapped in ascending order.

Recovery operation is a database process that occurs when a database first restarts after a downtime due to user initiated or system side operation. This rolls back all your in-flight but uncommitted transactions at the time of restart, and during this time the database becomes unavailable.
<!--/issueDescription-->

## **Recommended Steps**

Depending on the size of transactions to rollback, this activity takes time proportional to the size of the active transactions. Once this recovery operation is complete, your database(s) <!--$affectedDatabases-->affectedDatabases<!--/$affectedDatabases--> should become available.

Wait for REDO to complete the scan and make the database available again.
