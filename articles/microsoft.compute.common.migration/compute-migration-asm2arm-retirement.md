<properties
	pageTitle="Migration and Move/Guidance regarding retirement of Classic IAAS resources (ASM)"
	description="Migration and Move/Guidance regarding retirement of Classic IAAS resources (ASM)"
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="scottazure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32731147"
	resourceTags=""
	productPesIds="14749,15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="f19125d0-6031-47ed-b63f-26fd7c8ad960"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Migration and Move/Guidance regarding retirement of Classic IAAS resources (ASM)

4 out of 5 customers resolved their issue using the guides listed below.<br>

## Migrate your IaaS resources to Azure Resource Manager by March 1, 2023

In 2014, we launched IaaS on Azure Resource Manager, and have been enhancing capabilities ever since. Because it replaces IaaS resources from Azure Service Manager (ASM), we have started a 3 year retirement process for classic VMs beginning February 24th, 2020 and ending on March 1, 2023.<br>

If you use IaaS resources from ASM, please start planning today and complete migration by March 1, 2023. We encourage you to make the switch sooner to take all the advantages of [Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/management/).<br>

### How does this affect me?

1) On March 1st, 2023, all active Classic VMs will be stopped & deallocated but will not be deleted immediately.<br>

2) On March 1st, 2023, we will notify remaining subscriptions who have not migrated to Azure Resource Manager about our timelines for deleting any remaining Classic VMs.

The following Azure services and functionality will **NOT** be impacted by this retirement:<br>
- Cloud Services<br>
- Storage accounts **not** used by classic VMs<br>
- Virtual networks (VNets) **not** used by classic VMs.<br>

### What actions should I take?

Start planning for the migration to Azure Resource Manager, today. [Learn more](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-overview) about migrating your classic Linux and Windows VMs to Azure Resource Manager.<br>

For additional information, refer to the [Frequently asked questions about classic to Azure Resource Manager migration](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-faq)<br>

### Next steps

Create a plan to migrate your classic [Linux](https://docs.microsoft.com/azure/virtual-machines/migration-classic-resource-manager-plan?toc=/azure/virtual-machines/linux/toc.json) or [Windows](https://docs.microsoft.com/azure/virtual-machines/migration-classic-resource-manager-plan?toc=/azure/virtual-machines/windows/toc.json) VMs to Resource Manager.

## **Recommended Documents**

* [Frequently asked questions about migration of IaaS resources](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-faq?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Review most common migration errors](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-errors?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Review community tools for assisting with migration of IaaS resources](https://docs.microsoft.com/azure/virtual-machines/migration-classic-resource-manager-community-tools?toc=/azure/virtual-machines/windows/toc.json)<br>
* [Overview of platform-supported migration](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-overview?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Technical deep dive on platform-supported migration](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-deep-dive?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Planning for migration of IaaS resources from classic to Azure Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-plan?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Review the instructions on how to migrate using Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-ps?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Review the instructions on how to migrate using Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-cli?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Migrate ExpressRoute circuits and associated virtual network](https://docs.microsoft.com/azure/expressroute/expressroute-migration-classic-resource-manager)<br>
* [Migrate your VPN Gateway classic to Resource Manager](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-classic-resource-manager-migration)
