<properties
	pageTitle="wlextpluginservicestarttimedout"
	description="wlextpluginservicestarttimedout"
	infoBubbleText="extension plugin time out"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-wlextpluginservicestarttimedout"
	diagnosticScenario="azurebackup-crc-wlextpluginservicestarttimedout"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error WLExtPluginServiceStartTimedOut

<!--issueDescription-->
We have identified that your backup operation failed because of the following reasons.
<!--/issueDescription-->

## **Recommended steps**

1. The database might be offline. Ensure that it's is online and running.
2. [Check if there is an antivirus software blocking installation of plug-in](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#troubleshoot-backup-and-recovery-issues)
3. Ensure the latest VM guest agent is installed and is in running state.
