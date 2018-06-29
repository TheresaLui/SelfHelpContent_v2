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

- [Ensure Microsoft Azure Recovery Services (MARS) Agent is up to date before troubleshooting further](https://go.microsoft.com/fwlink/?linkid=229525&clcid=0x409) <br>
- [Ensure there is network connectivity between MARS agent and Azure](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup) <br>
- Ensure Microsoft Azure Recovery Services is running (in services.msc). If required restart and retry the operation <br>
- [Ensure 5-10% free volume space is available on scratch folder location](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder-br) <br>
- [Check if another process or antivirus software is interfering with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup) 
- [Scheduled backup fails, but manual backup works](https://aka.ms/ScheduledBackupFailManualWorks) <br>
- Ensure your OS has the latest updates <br>
- [Troubleshooting common Azure Backup agent issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot) <br>
