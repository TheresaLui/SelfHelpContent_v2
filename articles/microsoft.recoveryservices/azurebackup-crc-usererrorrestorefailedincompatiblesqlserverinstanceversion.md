<properties
	pageTitle="UserErrorRestoreFailedIncompatibleSQLServerInstanceVersion"
	description="UserErrorRestoreFailedIncompatibleSQLServerInstanceVersion"
	infoBubbleText="Restore failed as the SQL Server versions of the source instance and the target instance are incompatible."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorrestorefailedincompatiblesqlserverinstanceversion"
	diagnosticScenario="azurebackup-crc-usererrorrestorefailedincompatiblesqlserverinstanceversion"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorRestoreFailedIncompatibleSQLServerInstanceVersion

<!--issueDescription-->
We have identified that your restore failed as the source SQL Server version on which the backup was taken is incompatible with the target SQL Server.
<!--/issueDescription-->

## **Recommended Document**
This issue happens when the target SQL Server version on which restore operation is to be performed has lower SQL Server version than the source SQL Server where the backup was taken. To resolve this issue, perform any of of the below steps:

* Choose a target [SQL Server Instance](https://docs.microsoft.com/azure/virtual-machines/windows/sql/quickstart-sql-vm-create-portal) whose major version is greater than the SQL Server Instance from which backups were taken.
* [Upgrade the current SQL Server Instance](https://docs.microsoft.com/sql/database-engine/install-windows/upgrade-sql-server-using-the-installation-wizard-setup?view=sql-server-2017).
