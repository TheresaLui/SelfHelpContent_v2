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
  	cloudEnvironments="public,blackForest,fairfax,mooncake"
  	articleId="sqlmanagedinstance-connectivity-long-recovery"
  />

  # Managed Instance - Long recovery

  ## We ran diagnostics on your resource and found an issue

  <!--issueDescription-->
  We identified database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> was going through a long recovery.
  It started at <!--$recoveryStart-->recoveryStart<!--/$recoveryStart--> and lasted for <!--$recoveryDuration-->recoveryDuration<!--/$recoveryDuration-->.

  Recovery operation is a database process that occurs when a database first restarts after a downtime due to user initiated or system side operation. This rolls back all your in-flight but uncommitted transactions at the time of restart, and during this time the database becomes unavailable.
  <!--/issueDescription-->

  ## **Recommended Steps**

  Depending on the size of transactions to rollback, this activity takes time proportional to the size of the active transactions. Once this recovery operation is complete, your database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> should become available.

  Just wait for REDO to complete the scan and make the database available again.
