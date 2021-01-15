<properties
	pageTitle="Issue with moving vault"
	description="Issue with moving vault"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632781"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="77a4ff97-36eb-4d69-91b0-03d5e48989df"
	ownershipId="StorageMediaEdge_Backup"
/>

# Issue with moving vault

Resolve issues with moving a vault using the following resources. Make sure to review [prerequisites for moving a vault](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#prerequisites-for-moving-recovery-services-vault).

## **Recommended Steps**
- [Change vault configuration from GRS to LRS](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)
- [Supported regions](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#supported-regions) and [Prerequisites](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#prerequisites-for-moving-recovery-services-vault) to move a Recovery Services vault
- Move operation is allowed for vaults that only contain backup items. If it contains Azure Site Recovery items, the move operation is not supported.
- How to move a vault between [subscriptions](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription), or between [resource groups](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group)
- [Can I move backup data/protected items to another vault?](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#can-i-move-backup-data-to-another-vault)
- [How can I move data from the Recovery Services vault to on-premises?](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#how-can-i-move-data-from-the-recovery-services-vault-to-on-premises)
- [Move an Azure virtual machine to a different Recovery Services Vault](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#move-an-azure-virtual-machine-to-a-different-recovery-service-vault)
- [Move Azure resources to another Azure subscription or to another resource group under the same subscription](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription)

## **Recommended Documents**

- [How to use PowerShell to move a vault?](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-powershell-to-move-recovery-services-vault)
