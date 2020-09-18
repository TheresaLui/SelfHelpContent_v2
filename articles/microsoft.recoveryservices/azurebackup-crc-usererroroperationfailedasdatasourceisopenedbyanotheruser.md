<properties
	pageTitle="UserErrorOperationFailedAsDatasourceIsOpenedByAnotherUser"
	description="UserErrorOperationFailedAsDatasourceIsOpenedByAnotherUser"
	infoBubbleText="Connection to datasource is already open and can only have one user connected at a time."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererroroperationfailedasdatasourceisopenedbyanotheruser"
	diagnosticScenario="azurebackup-crc-usererroroperationfailedasdatasourceisopenedbyanotheruser"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorOperationFailedAsDatasourceIsOpenedByAnotherUser

<!--issueDescription-->
We have identified that the database operation failed due to another session connected to database, which is not allowing the operation to be triggered.
<!--/issueDescription-->

## **Recommended Steps**

* Use the [sp_who](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-who-transact-sql?view=sql-server-2017) or sp_who2 stored procedures to find the active processes in the database
* Kill all the active process in the database (if not risky)
* Retrigger the backup operation
