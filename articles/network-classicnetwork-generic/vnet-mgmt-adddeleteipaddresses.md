<properties
	pageTitle="management/addordeleteipaddressestoavnet"
	description="management/addordeleteipaddressestoavnet"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="anavin"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584248"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# management/addordeleteipaddressestoavnet

## **Recommended steps**
- Unable to successfully add additional IPs to your VM's network interface (NIC)? After you have added multiple IP addresses to your NIC via Portal or PowerShell, you must add them to the VM's OS. See our [step by step guide](https://docs.microsoft.com/azure/virtual-network/virtual-network-multiple-ip-addresses-portal#os-config) on how to do this.

- You may not be able to add or delete IP addresses to a VNet if it has peerings with other VNet. Learn how to add or delete [here](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-network#add-address-spaces)<br>

- Unable to delete a VNet? Your VNet may be locked by your organization. [You can create or delete the lock.](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#who-can-create-or-delete-locks-in-your-organization)<br>


## **Recommended documents**
[Create, change or delete a virtual network subnet](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet) <br>
[Add/Delete multiple IPs to your NIC](https://docs.microsoft.com/azure/virtual-network/virtual-network-multiple-ip-addresses-portal)