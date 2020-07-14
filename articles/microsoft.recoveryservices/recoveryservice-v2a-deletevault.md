<properties
	pageTitle="Delete a vault in V2A"
	description="Delete a vault in V2A"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="v-bllydi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32592050"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="b6e56f6d-5f12-4627-801b-f7b0a0638073"
	ownershipId="Compute_SiteRecovery"
/>

# Delete a vault in V2A scenario

## **Recommended steps**

- [Step-by-step approach to delete a Recovery Services vault](https://docs.microsoft.com/azure/site-recovery/delete-vault#delete-a-site-recovery-vault-1)<br>
- [**Force delete the vault using Powershell** ](https://docs.microsoft.com/azure/site-recovery/delete-vault#use-powershell-to-force-delete-the-vault) if any components can't be removed <br>
- [Disable replication for all protected items](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure) before attempting to delete a vault <br>
- Use **Remove** to [disable replication if source environment is not accessible](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure)<br>
- [Delete all replication policies](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-replication#disassociate-or-delete-a-replication-policy) before attempting to delete a vault <br>
- [Delete references to any registered vCenter](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-vcenter#delete-a-vcenter-server) before attempting to delete a vault <br>
- [Delete all registered configuration servers](https://docs.microsoft.com//azure/site-recovery/vmware-azure-manage-configuration-server#delete-or-unregister-a-configuration-server) before attempting to delete a vault <br>
