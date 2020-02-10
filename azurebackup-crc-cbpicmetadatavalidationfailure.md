<properties
	pageTitle="CBPIcMetadataValidationFailure"
	description="CBPIcMetadataValidationFailure"
	infoBubbleText="MARS agent has detected inconsistencies while verifying the latest backup. A new recovery point could not be created."
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
	cloudEnvironments="public"
/>

# Error CBPFilePathIsNonexistent

<!--issueDescription-->
We have identified that your backup operation is stuck or failed in the metadata phase while verifying integrity check. 
<!--/issueDescription-->

## **Recommended Steps**

* If you notice an ongoing backup (that is stuck), then try cancelling the job.
* Ensure there is enough space for shadow storage and free disk space.
* Restart the MARS agent
* Disable the short names in the system using *fsutil 8dot3name set 1* from command and then retry the backup operation.
* Wait for the next schedule backup to trigger.
