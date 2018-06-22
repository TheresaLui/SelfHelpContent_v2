<properties
	pageTitle="Backup failures while using Azure Backup agent"
	description="Common issues during backup of files and folders using Azure Backup agent"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="pvrk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553275"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, MoonCake"
/>

# Backup of files and folders with Azure Backup Agent fails

## **Recommended Steps**

To resolve common isuess, try one or more of the following steps.

**Azure Backup service and Microsoft Azure Recovery Services Agent versions do not match (0x1FBD3)** <br>
If your backup jobs are failing with above error then [follow these steps](https://go.microsoft.com/fwlink/?linkid=229525) to resolve.<br>

## **Scheduled backup failed** <br>
•	Follow [these steps](https://aka.ms/ScheduledBackupFailManualWorks) to troubleshoot and resolve the issue<br>
•	Download and install the latest agent from [here](http://aka.ms/azurebackup_agent)<br>
•	Verify whether Windows Guest Agent service is running in services (services.msc). Try restart the Windows Guest Agent service and initiate the Backup.<br>

## **The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup** <br>
•	Check network connectivity to Azure using steps listed in [this article](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup), fix issues if any and then reinitiated the backup jobs.<br>
•	If you have Antivirus software running on the same system, it might be blocking the backups from happening. Test by temporarily disabling the Anti-virus, reinitiate to see if backups are working fine. If you find this to be the reasons, then from your Antivirus product exclude the folders using steps listed in [this article](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup).<br>

## **Microsoft Azure Backup failed to access the shadow copy because of inadequate disk space on the volume**<br>
•	Ensure that the cache volume has free space corresponding to 5-10 percentage of the backup data size or at least 2.5GB, whichever is greater.<br>
•	If required, switch to a new cache location that meets the specified space requirements. Refer to [this article](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#backup) for **changing the cache location** to a different volume with recommended disk size.<br>
•	Ensure scratch folder is not located on OS volume.<br>

If above recommendations does not resolve your issue, then post questions your question to [Azure Backup discussion forum](https://social.msdn.microsoft.com/forums/azure/home?forum=windowsazureonlinebackup).
