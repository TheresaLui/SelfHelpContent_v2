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

## **Recommended Steps**
- Certain configuration can prevent moving VM(s) across subscriptions. Review this [article](https://docs.microsoft.com/azure/azure-resource-manager/management/move-limitations/virtual-machines-move-limitations#virtual-machines-with-azure-backup) to verify if your scenario is unsupported Review and the workaround steps to move the VMs. 
- You must meet the prerequisites listed in this [article](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#prerequisites-for-moving-recovery-services-vault) before moving resources across subscription/resource group. 
- Move is allowed for vaults that only contain backup items (if it has ASR items that move is not supported) 


## **Recommended Documents**

- [Prerequisites for moving a vault](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#prerequisites-for-moving-recovery-services-vault)<br>
- [Use PowerShell to move a vault](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-powershell-to-move-recovery-services-vault)<br>
- [Move a vault between subscriptions](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription)<br>
- [Move a vault between Resource Groups](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group)<br>
