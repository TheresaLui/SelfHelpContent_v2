<properties
	pageTitle="Azure Windows VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32553299"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Azure Windows VM Restore Limitations

## **Recommended Steps**
**Frequently Asked Questions:**<br>
- [*How can I restore specific files or folders from IaaS VM?*](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)<br>
- *How to restore to latest/specific recovery point using* - [Portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#select-a-restore-point-for-restore), [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm) or [Restored disk](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)<br>
- [*How to configure static IP address to restored VM?*](https://docs.microsoft.com/azure/virtual-network/virtual-networks-reserved-private-ip#how-to-add-a-static-internal-ip-to-an-existing-vm)<br>
- [*How to restore an Encrypted VM?*](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption)<br>
- [*How to restore when Key (Key Encryption Key) and Secret (BitLocker Encryption Key) does not exist in the key vault?*](https://docs.microsoft.com/azure/backup/backup-azure-restore-key-secret)<br>
- [*How to restore a Domain Controller VM?*](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-domain-controller-vms)<br>
- *How can I attach existing NIC to the restored VM?* [Step 1](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-remove-nic) remove from original VM and [Step 2](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-add-nic) to attach to restored VM.<br>
- [*How to restore VM with special network configurations?*](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-vms-with-special-network-configurations)<br>

**Limitations**<br>
- Restoring backed-up VMs across Zone, Region, subscription or V-Net is not supported.<br>
- [File/Folder restore limitation with special configuration - **Dynamic Disks, Storage Spaces**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#special-configurations) <br>

**Common Errors and Workarounds**<br>
- If you are **unable to restore**, verify that you don’t have any group policy restriction in place from portal.<br>
- If you are **unable to see backup items** from the portal then ensure you have [required permission](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault) to access backup vault. <br>
- [Ensure appropriate Role Based Access controls in place.](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault) <br>
- [Restore failed with Cloud Internal error](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#restore)<br>
- [The selected DNS name is already taken](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#restore)<br>
- [The specified virtual network configuration is not correct](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#restore)<br>
- [The specified cloud service is using a reserved IP](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#restore)<br>

## **Recommended documents**
- [Azure virtual machine restore troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#backup-or-restore-taking-time)<br>
- [How to restore virtual machine using portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)<br>
- [How to restore virtual machine using PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm)<br>
