<properties
	pageTitle="CBPIcMetadataValidationFailure"
	description="CBPIcMetadataValidationFailure"
	infoBubbleText="MARS agent has detected inconsistencies while verifying the latest backup"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpicmetadatavalidationfailure.md"
	diagnosticScenario="azurebackup-crc-cbpicmetadatavalidationfailure.md"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPIcMetadataValidationFailure

<!--issueDescription-->
We have identified that your backup operation is stuck or failed in the metadata phase while verifying integrity check. 
<!--/issueDescription-->

## **Recommended Steps**

* If you notice an ongoing backup appears stuck, then try cancelling the job
* Ensure there is enough space for shadow storage and free disk space
* Restart the MARS agent
* Disable the short names in the system using `fsutil 8dot3name set 1` from the command prompt and then retry the backup operation
* Wait for the next schedule backup to trigger
