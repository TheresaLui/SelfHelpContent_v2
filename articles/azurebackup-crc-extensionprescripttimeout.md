<properties
	pageTitle="ExtensionPreScriptTimeout"
	description="ExtensionPreScriptTimeout"
	infoBubbleText="Execution of App-Consistent Backup Pre-Script timed-out."
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
	cloudEnvironments="public"
/>

# ExtensionPreScriptTimeout

<!--issueDescription-->
## **Snapshot operation failed as snapshot limit has exceeded for some of the disks attached**
<!--/issueDescription-->

## **Recommended Steps**
During backup pre-check, user will encounter a warning that pre/post script timed-out for the app consistency, however the backup succeed for the File System consistency.<br/>
As the default timeout for each script (pre and post script) is 30 seconds, if it take more than 30 sec then increase the time out as per the script running time.

**To change the timeout**:

In the Linux window go to the /etc/azure path and edit the **VMSnapshotScriptPluginConfig.json** file with the approximate time out value required to complete the script.

> [!NOTE]
> Maximum value of timeout is 1800 seconds (30 minutes), for more information refer this [article](https://docs.microsoft.com/azure/backup/backup-azure-linux-app-consistent#steps-to-configure-pre-script-and-post-script).
