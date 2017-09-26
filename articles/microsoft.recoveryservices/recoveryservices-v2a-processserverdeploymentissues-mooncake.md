<properties
	pageTitle="Site Recovery (VMware to Azure)/Process Server deployment issues"
	description="Site Recovery (VMware to Azure)/Common issues during Process Server deplooyments"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="AnoopVasudavan"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536429"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
/>

# Site Recovery (VMware to Azure)/ Process Server deployment and issues.

Common issues during Process Server deployment

## **Recommended Steps**
* Ensure that the Process Server is deployed in the same network as the virtual machines you want to protect/re-protect.
* If you are deploying an Process Server in Azure, ensure you choose the correct deployment model for your process server. Resource manager virtual machines cannot be Re-protected by a Classic model Process Server and vice versa.
* If you are deploying a Process Server in Azure, ensure you [register it with the Configuration Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-setup-azure-ps-resource-manager#registering-the-process-server-running-in-azure-to-a-configuration-server-running-on-premises) before you proceed to use it for Re-protecting virtual machines.

## **Recommended Documents**
* [Deploy a Process Server(Resource Manager) in Azure for Failback](https://docs.azure.cn/site-recovery/site-recovery-vmware-setup-azure-ps-resource-manager)
* [Deploy a Process Server(Classic) in Azure for Failback](https://docs.azure.cn/site-recovery/site-recovery-vmware-setup-azure-ps-classic)
* [Deploy a on-premises Scale-out Process Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server)
* [Registering a Process Server (running in Azure) to a Configuration Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-setup-azure-ps-resource-manager#registering-the-process-server-running-in-azure-to-a-configuration-server-running-on-premises)
* [Re-registering a Scale-out Process Server (running on-premises) to a Configuration Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server#re-registering-a-scale-out-process-server)
* [Decommissioning a Scale-out Process Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server#decommissioning-a-scale-out-process-server)
* [Unregistering a disconnected Process Server](https://docs.azure.cn/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server#unregistering-a-disconnected-scale-out-process-server-from-a-configuration-server)
