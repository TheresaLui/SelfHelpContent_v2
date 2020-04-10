<properties
	pageTitle="UserErrorOperationNotAllowedDatabaseMirroringEnabled"
	description="UserErrorOperationNotAllowedDatabaseMirroringEnabled"
	infoBubbleText="Backup of databases participating in a database mirroring session is not supported by AzureWorkloadBackup."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererroroperationnotalloweddatabasemirroringenabled"
	diagnosticScenario="azurebackup-crc-usererroroperationnotalloweddatabasemirroringenabled"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorOperationNotAllowedDatabaseMirroringEnabled

<!--issueDescription-->
We have identified that your operation failed because Azure backup does not support mirror databases and database snapshots for backup and restore operations.
<!--/issueDescription-->

## **Recommended Steps**

* To resolve this issue, remove the database mirroring session of the database for the operation to complete successfully
* Alternatively, if the database is already protected, then **Stop backup** operation on the database
