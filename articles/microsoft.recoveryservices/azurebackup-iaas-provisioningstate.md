<properties
	pageTitle="Diagnose and resolve issues with Windows Azure virtual machine ProvisioningStateFailed"
	description="Diagnose and resolve issues with Windows Azure virtual machine ProvisioningStateFailed"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684548"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="baa7233f-a514-4b71-aa34-096a5f6ab0c5"
	ownershipId="StorageMediaEdge_Backup"
/>

# Diagnose and resolve issues with Windows Azure ProvisioningStateFailed

## **Recommended Steps**
If your backup operation fails with *UserErrorVmProvisioningStateFailed - The VM is in failed provisioning state*, this could be due to one of the extension status might be in **Provisioning failed** state. To resolve this issue:

- Ensure the Virtual machine is in Running state
- Open *Azure Portal > VM > Settings > extensions >* and ensure all extension's status are in **Provisioning succeeded** state. If you notice **Provisioning failed** state, then remove that **Provisioning failed** extension and try restarting the virtual machine.

## **Recommended Documents**
-  [Common VM backup errors](https://go.microsoft.com/fwlink/?linkid=2107503)
