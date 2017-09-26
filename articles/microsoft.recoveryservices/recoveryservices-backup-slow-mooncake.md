<properties
	pageTitle="Windows Backup to Azure Backup/Schedule backup for a Windows Server or a client"
	description="Windows Backup to Azure Backup/Schedule backup for a Windows Server or a client"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="kasparks"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553280"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
/>

# Windows Backup to Azure Backup/Schedule backup for a Windows Server or a client

If you are facing issues with your Windows server files and folders backups being very slow, please try one or more of the below steps

## **Recommended steps**

* Server being backed up is facing  performance limitations causing backup to be slow <br>
[Performance counters and recommended ranges for optimal backup](https://docs.azure.cn/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause1)

* Another process or antivirus interfering with Azure Backup causing backup to be slow or even fail <br>
[Steps to ensure there are no conflicts with another process or antivirus](https://docs.azure.cn/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause2)

* Backing up individual files and folders in an Azure IaaS VM is very slow <br>
[Steps to optimize performance for Azure VM](https://docs.azure.cn/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause3)

* Backup large number (multi-million) of small files is very slow <br>
[Steps to understand bottlenecks in the case of large number of files](https://docs.azure.cn/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause4)

## **Recommended documents**
[Step by step guide to setup files and folder backup using Azure Backup Agent](https://docs.azure.cn/backup/backup-configure-vault)
