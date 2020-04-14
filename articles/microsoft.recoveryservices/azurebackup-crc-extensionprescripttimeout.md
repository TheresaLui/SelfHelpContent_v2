<properties
	pageTitle="ExtensionPreScriptTimeout"
	description="ExtensionPreScriptTimeout"
	infoBubbleText="Execution of App-Consistent Backup Pre-Script timed-out"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-extensionprescripttimeout"
	diagnosticScenario="azurebackup-crc-extensionprescripttimeout"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

#  Error ExtensionPreScriptTimeout

<!--issueDescription-->
We have identified that your backup operation failed due to pre/post script time-out with error ExtensionPreScriptTimeout. The snapshot operation failed, as snapshot limit has exceeded for some of the disks attached.
<!--/issueDescription-->

## **Recommended Steps**

During backup pre-check, user will encounter a warning that pre/post script timed-out for app consistency. However, the backup succeeded for the File System consistency. The default timeout for each script (pre and post script) is 30 seconds. If the script takes longer than 30 seconds, increase the time out value per the script running time. 

## Change the Time Out Value

In the Linux window, go to the `/etc/azure` path and edit the `VMSnapshotScriptPluginConfig.json` file. Update the time out value and save the file. 

[!NOTE] [Maximum value of timeout](https://docs.microsoft.com/azure/backup/backup-azure-linux-app-consistent#steps-to-configure-pre-script-and-post-script) is 1800 seconds (30 minutes).
