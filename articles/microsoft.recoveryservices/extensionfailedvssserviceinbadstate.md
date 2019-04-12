<properties
	pageTitle="ExtensionFailedVssServiceInBadState"
	description="ExtensionFailedVssServiceInBadState"
	infoBubbleText="Snapshot operation failed due to VSS Writers in bad state"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-extensionfailedvssserviceinbadstate"
	diagnosticScenario="azurebackup-crc-extensionfailedvssserviceinbadstate"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ExtensionFailedVssWriterInBadState

<!--issueDescription-->
## **Snapshot operation failed due to VSS (Volume Shadow Copy) service in bad state**
<!--/issueDescription-->

## **Recommended Steps**
We have detected that you’re VSS (Volume Shadow copy Service) service is in an inconsistent state.<br/>
To resolve this issue, restart the VSS and retry the backup operation.
