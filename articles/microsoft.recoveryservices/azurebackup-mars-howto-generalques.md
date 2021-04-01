<properties
	pageTitle="Files and folder backup How-to and general questions"
	description="Files and folder backup How-to and general questions"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathvasireddy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32612995"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2cca467c-ba08-41e2-a736-bad2fab878e9"
	ownershipId="StorageMediaEdge_Backup"
/>
# Backup Files & Folders using Azure Backup agent

## **Recommended Documents**

## Configuration

- How to configure [Backup for Files and Folders using Azure Backup Agent?](https://docs.microsoft.com/azure/backup/backup-windows-with-mars-agent)
- What are the [Network and Connectivity Requirements for Files and Folders Backup](https://docs.microsoft.com/en-us/azure/backup/backup-windows-with-mars-agent#verify-internet-access)
- Where can i find the [MARS Agent supported configurations and limitations matrix](https://docs.microsoft.com/azure/backup/backup-support-matrix-mars-agent)
- Where is my [scratch folder](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#how-to-check-if-scratch-folder-is-valid-and-accessible)?
- How can I [change my scratch folder location](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#how-do-i-change-the-cache-location-for-the-mars-agent)?
- How to [identify servers with older agent versions and upgrade](https://docs.microsoft.com/azure/backup/upgrade-mars-agent)?
- How to [remove a server protected by Azure Backup Agent](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#delete-protected-items-on-premises)?

##Backup

- [How does MARS backup work](https://docs.microsoft.com/azure/backup/backup-architecture#architecture-direct-backup-of-on-premises-windows-server-machines-or-azure-vm-files-or-folders)
- [Can I backup an Azure VM using MARS Agent?](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#can-i-use-the-mars-agent-to-back-up-files-and-folders-on-an-azure-vm)
- [What are the backup options for On-Premises and Azure VMs](https://docs.microsoft.com/azure/backup/backup-architecture#how-does-azure-backup-work)
- [How can I **stop** my Azure Backup Agent backups](https://docs.microsoft.com/azure/backup/backup-azure-manage-mars#stop-protecting-files-and-folder-backup)?
- [How can I **stop backing up specific files and folders** using an exclusion rule](https://docs.microsoft.com/azure/backup/backup-azure-manage-mars#add-exclusion-rules-to-existing-policy)?

##Restore

- How to restore files to: [**original location**](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-recover-data-to-the-same-machine) (or) [**alternative location**?](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-restore-data-to-an-alternate-machine)<br>
- [I have lost my original machine. How can i restore the backed up data?](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#how-do-i-recover-if-i-lost-my-original-machine-where-backups-were-taken)
- [I have lost/forgotten my passphrase. What are my options?](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#can-i-recover-if-i-forgot-my-passphrase)

##Monitor

- [How to monitor Backup Jobs?](https://docs.microsoft.com/azure/backup/backup-azure-manage-windows-server#monitor-backup-jobs-and-alerts)<br>
- [How to setup Alerts for Backup?](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#backup-alerts-in-recovery-services-vault)<br>
- [How to see all Backup Items in the vault?](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#backup-items-in-recovery-services-vault)<br>
- [How to determine backup items storage consumption?](https://docs.microsoft.com/azure/backup/configure-reports#backup-items)

## Other generally useful links

- [Frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#configure-backups)<br>
- [Troubleshooting common Azure Backup Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)
