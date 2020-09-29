<properties
	pageTitle="Migration and Move/Migrate IAAS resources from Classic (ASM) to Azure Resource Manager (ARM)"
	description="Migration and Move/Migrate IAAS resources from Classic (ASM) to Azure Resource Manager (ARM)"
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="scottazure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32513964"
	resourceTags=""
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="d24bcf5a-b3ad-486c-86a2-bcf511139deb"
	ownershipId="Compute_VirtualMachines"
/>

# Migration and Move/Migrate IAAS resources from Classic (ASM) to Azure Resource Manager (ARM)

4 out of 5 customers resolved their issue using the guides listed below.<br>

**Frequently Asked Questions**

**What does this migration plan mean for my existing tooling?**<br>
Updating your tooling to the Resource Manager deployment model is one of the most important changes that you have to account for in your migration plans.<br>

**How long will the management-plane downtime be?**<br>
It depends on the number of resources that are being migrated. For smaller deployments (a few tens of VMs), the whole migration should take less than an hour. For large-scale deployments (hundreds of VMs), the migration can take a few hours.<br>

**Can I roll back after my migrating resources are committed in Resource Manager?**<br>
You can abort your migration as long as the resources are in the prepared state. Rollback is not supported after the resources have been successfully migrated through the commit operation.<br>

**Can I roll back my migration if the commit operation fails?**<br>
You cannot abort migration if the commit operation fails. All migration operations, including the commit operation, are idempotent. So we recommend that you retry the operation after a short time. If you still face an error, create a support ticket or create a forum post with the ClassicIaaSMigration tag on our VM forum.<br>

**What happens if I run into a quota error while preparing the IaaS resources for migration?**<br>
We recommend that you abort your migration and then log a support request to increase the quotas in the region where you are migrating the VMs. After the quota request is approved, you can start executing the migration steps again.<br>

## **Recommended Documents**

* [Frequently asked questions about migration of IaaS resources](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-faq?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
* [Review most common migration errors](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-errors?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
* [Overview of platform-supported migration](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-overview?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
* [Technical deep dive on platform-supported migration](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-deep-dive?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
* [Planning for migration of IaaS resources from classic to Azure Resource Manager](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-plan?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Review the instructions on how to migrate using Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-cli?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
* [Migrate ExpressRoute circuits and associated virtual network](https://docs.microsoft.com/azure/expressroute/expressroute-migration-classic-resource-manager)<br>
* [Migrate your VPN Gateway classic to Resource Manager](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-classic-resource-manager-migration)