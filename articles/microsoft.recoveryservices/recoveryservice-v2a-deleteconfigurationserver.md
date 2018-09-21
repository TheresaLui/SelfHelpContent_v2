<properties
	pageTitle="Delete a configuration server V2A"
	description="Delete a configuration server V2A"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="v-bllydi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32592047"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
/>

# Delete a configuration server

## **Recommended steps**

- [Disable replication](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure) before deleting or unregistering a configuration server <br>
- Delete or unregister a configuration server (VMware) - [**through portal**](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#delete-or-unregister-a-configuration-server) or [**Powershell**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#delete-with-powershell)<br>
- Re-register a configuration server (VMware) - [to the **same vault**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#reregister-a-configuration-server-in-the-same-vault) or [to a **different vault**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#register-a-configuration-server-with-a-different-vault)<br>
- Delete or unregister a configuration server (Physical) - [**through portal**](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#delete-or-unregister-a-configuration-server) or [**Powershell**](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#delete-or-unregister-a-configuration-server-powershell)<br>
- Re-register a configuration server (Physical) - [to the **same vault**](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#reregister-a-configuration-server-with-the-same-vault) or [to a **different vault**](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#register-a-configuration-server-with-a-different-vault)<br>
- Use **Remove** to [disable replication if source environment is not accessible](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure)<br>

## **Recommended documents**

- [How to disable replication/ASR components and delete a Recovery Services vault?](https://docs.microsoft.com/azure/site-recovery/delete-vault#delete-a-site-recovery-vault-1)<br>
- [How to **force delete the vault using powershell?**](https://docs.microsoft.com/azure/site-recovery/delete-vault#use-powershell-to-force-delete-the-vault)
