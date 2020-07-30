<properties
	pageTitle="Azure IAAS VM Backup Configure Protection"
	description="Azure IAAS VM Backup Configure Protection failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="kasparks"
	ms.author="kasparks"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553285"
	resourceTags=""
	productPesIds="15207"
	articleId="95333929-5668-4cb5-bed3-3855436ddbf7"
	cloudEnvironments="public, fairfax, usnat, ussec"
		ownershipId="StorageMediaEdge_Backup"
/>

# Unable to Configure Backup for Azure Virtual Machines

## **Recommended Documents**

- [How can I modify the retention period?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#manage-backup-policy-for-a-vm)
- [What happens to the existing recovery points if I change the retention policy?](https://docs.microsoft.com/azure/backup/backup-architecture#backup-policy-essentials)
- [How do I take multiple backups on the same day?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#run-an-on-demand-backup). **Scheduled backup** is limited to one per day, for multiple backups use on-demand backup as workaround.  
- [Can I exclude disks that I do not want to backup?](https://azure.microsoft.com/updates/excludediskpreview/)
- [How long will the backup data be retained after I stop backup?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)
- [How to stop backup on my VM and delete all the recovery points?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)
- [How to troubleshoot permission issues during configure protection?](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault)
- [How to enable cross region restore?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#set-cross-region-restore)
- How to configure protection through [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation) and [Azure automation](https://docs.microsoft.com/azure/backup/backup-rm-template-samples)
- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
