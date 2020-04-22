<properties
	pageTitle="UserErrorSQLVDIInitFailed"
	description="UserErrorSQLVDIInitFailed"
	infoBubbleText="SQL VDI initialization has failed."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorsqlvdiinitfailed"
	diagnosticScenario="azurebackup-crc-usererrorsqlvdiinitfailed"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorSQLVDIInitFailed

<!--issueDescription-->
We have identified that your backup operations failed due to the VDI associated with the SQL Instance is in an inconsistent state.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the below:

* Check if binary sqlvdi.dll is properly registered in Windows. Re-register if necessary.
* Check if database has some DBCC errors. Run the query `DBCC CHECKDB (DatabaseName) WITH NO_INFOMSGS, ALL_ERRORMSGS` in SQL Server Management Studio, and fix the errors if any
* Try repairing installation of the SQL instance associated with the database
