<properties
	pageTitle="Windows Backup to Azure Backup/Schedule backup for a Windows Server or a client"
	description="Windows Backup to Azure Backup/Schedule backup for a Windows Server or a client"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32447383"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Windows Backup to Azure Backup/Schedule backup for a Windows Server or a client

If you are facing issues with your Windows server files and folders backups being very slow, please try one or more of the below steps

## **Recommended steps**

* Server being backed up is facing  performance limitations causing backup to be slow <br>
[Performance counters and recommended ranges for optimal backup](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue/#cause-1-backup-slow-due-to-performance-bottlenecks-on-the-computer-thats-being-backed-up)

* Another process or antivirus intefering with Azure Backup casuing backup to be slow or even fail <br>
[Steps to ensure there are no conflicts with another process or antivirus](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue/#cause-2-another-process-or-antivirus-software-is-interfering-with-the-azure-backup-process)

* Backing up individual files and folders in an Azure IaaS VM is very slow <br>
[Steps to optimize performance for Azure VM](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue/#cause-3-the-backup-agent-is-running-in-an-azure-virtual-machine-vm)

* Backup large number (multi-million) of small files is very slow <br>
[Steps to understand bottlenecks in the case of large number of files](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue/#cause-4-backing-up-a-large-number-multi-millions-of-files)

* Step by step guide to setup files and folder backup using Azure Backup Agent <br>
[Configure backup vault](https://azure.microsoft.com/en-us/documentation/articles/backup-configure-vault/)
