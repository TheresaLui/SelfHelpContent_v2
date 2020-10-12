<properties
	pageTitle="networkvirtualappliance/paloaltonetworks"
	description="networkvirtualappliance/paloaltonetworks"
	service="microsoft.network"
	resource="virtualappliance"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632164"
	resourceTags=""
	productPesIds="16679"
	cloudEnvironments="public,mooncake,fairfax,blackforest, usnat, ussec"
	articleId="nva-paloaltonetworks.md"
	ownershipId="CloudNet_NVA"
/>

# networkvirtualappliance/paloaltonetworks

Use this support topic path for Azure specific issues (e.g. Virtual Network, UDR, NSG etc.) related to Virtual Appliances. If your issue is specific to a Virtual Appliance, please reach out to the respective Virtual Appliance provider (3rd party) for support. Virtual Appliance tickets raised here do not get routed to 3rd party support.

## **Recommended Steps**

* To get help from Palo Alto Networks, open a support request [here](https://support.paloaltonetworks.com)
* **Remote Work:** [Network Virtual Appliance (NVA) considerations for remote work](https://docs.microsoft.com/azure/vpn-gateway/nva-work-remotely-support)
* Check [troubleshooting for Network Virtual Appliance issues in Azure](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva) for additional details
* For intermittent/reliability issues
   * Check CPU, network and memory performance on the VM 'Overview’ page. If you are seeing high utilization sustained over time contact Palo Alto Networks by opening a support request [here](https://support.paloaltonetworks.com)
   * Restart the virtual machine to address application issues by selecting ‘Restart’ at the top of the VM resource blade
   * For further analysis from Palo Alto Networks, open a support request [here](https://support.paloaltonetworks.com)
* To understand your NVA’s network bandwidth do the following: 
   * In the Azure portal, go to the VM ‘Overview’ page and note the 'Size' property of your VM
   * Go [here](https://docs.microsoft.com/azure/virtual-machines/linux/sizes) to find your VM size, click on the correct VM ‘Type’ in the table, then click on the correct VM size
   * [Contact the NVA vendor directly](https://support.paloaltonetworks.com) for guidance on SKU sizing and bandwidth capabilities
