<properties
	pageTitle="ExtensionFailedVssServiceInBadState"
	description="ExtensionFailedVssServiceInBadState"
	service="microsoft.recoveryservices"
	infoBubbleText="Snapshot operation failed due to VSS Writers in bad state"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv""
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
## **Snapshot operation failed due to VSS (Volume Shadow Copy) service in bad state.**
<!--/issueDescription-->

## **Recommended Steps**
We have detected that you are currently running a VSS (Volume Shadow copy Service) service in bad state. To resolve this issue we need to restart VSS (Volume Shadow copy Service) service in bad state.<br>
To restart VSS from the elevated command prompt, run **vssadmin** list writers. The output contains out all the VSS service and their state.
