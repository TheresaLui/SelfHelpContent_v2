<properties
	pageTitle="Backup failures while using Azure Backup agent"
	description="Common issues during backup of files and folders using Azure Backup agent"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="pvrk"
	ms.author="pvrk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553275"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="fc3023bd-b8cf-4451-a14d-76e1a8ba8c15"
	ownershipId="StorageMediaEdge_Backup"
/>

# Backup of files and folders with Azure Backup Agent fails

## **Recommended Steps**

- **Job could not be started as another job was in progress** :
  - [Check steps to prevent job overlap](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#job-could-not-be-started-as-another-job-was-in-progress)
  - [Check if the previous job was running in unoptimized mode and is taking longer time](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-backup-job-running-in-unoptimized-mode)
- [Ensure your OS is supported and has the latest updates](https://docs.microsoft.com/azure/backup/backup-support-matrix-mars-agent#supported-operating-systems)
- [Ensure Microsoft Azure Recovery Services (MARS) Agent is up to date before troubleshooting further](https://docs.microsoft.com/azure/backup/upgrade-mars-agent)
- [Ensure there is network connectivity between MARS agent and Azure](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- Ensure Microsoft Azure Recovery Services is running (in Service console). If required restart and retry the operation
- [Ensure 5-10% free volume space is available on scratch folder location](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder), If you back up Windows System State, ensure there is 30-35 GB of free space in the volume containing the cache folder.
- [Check if another process or antivirus software is interfering with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup) 
- [Scheduled backup fails, but manual backup works](https://docs.microsoft.coms/azure/backup/backup-azure-mars-troubleshoot#backups-dont-run-according-to-schedule)
- [Troubleshooting common Azure Backup agent issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)

## **Recommended Documents**

- [Invalid vault credentials provided](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)<br>
- [Failed to download the vault credential file](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#unable-to-download-vault-credential-file)<br>
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)<br>
- [(407) Proxy Authentication Required](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)<br>
- [Failed to set the encryption key for secure backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups)<br>
- [Activation did not succeed completely but the encryption passphrase was saved to the following file](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups)<br>
- [Encryption passphrase not correctly configured](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#encryption-passphrase-not-correctly-configured)
