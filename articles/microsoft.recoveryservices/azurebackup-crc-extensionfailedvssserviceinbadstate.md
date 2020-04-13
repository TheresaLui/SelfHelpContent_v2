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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionFailedVssServiceInBadState

<!--issueDescription-->
We have detected that your VSS (Volume Shadow copy Service) service is in an inconsistent state.
<!--/issueDescription-->

## **Recommended Steps**

* Restart the VSS and retry the backup operation
- To restart the VSS services please refer to the [documentation](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionfailedvsswriterinbadstate---snapshot-operation-failed-because-vss-writers-were-in-a-bad-state)
