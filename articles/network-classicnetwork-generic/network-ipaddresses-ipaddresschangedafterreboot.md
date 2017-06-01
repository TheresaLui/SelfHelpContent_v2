<properties
	pageTitle="ipaddresses/ipaddresschangedafterreboot"
	description="ipaddresses/ipaddresschangedafterreboot"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="viorican"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32547250"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# ipaddresses/ipaddresschangedafterreboot

## Recommended documents
[IP Allocation method](https://azure.microsoft.com/documentation/articles/virtual-network-ip-addresses-overview-arm/#allocation-method)

## Frequently asked questions
### **Why are there missing IP addresses in my VNet?**
Azure reserves 5 IP addresses within each subnet. The first and last IP addresses of the subnets are reserved for protocol conformance, along with 3 more addresses used for Azure services.

### **Why can't I RDP to my VM?**
In order to be able to RDP into your VM, you need to have a public IP associated to your VM. To learn how to associate or create a public IP read the [Create a public IP address](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address#a-namecreateacreate-a-public-ip-address) article.


### **The IP address of my VM changed after reboot. How do I get the IP address back?**
Unfortunately, a lost IP address cannot be recovered. The reason for the change is the IP address is dynamic. **Dynamic** addresses are assigned only after the public IP address is associated to a NIC attached to a VM and the VM is started for the first time. Dynamic addresses can change if the VM the NIC is attached to is stopped (deallocated). **Static** addresses are assigned when the public IP address is created. Static addresses do not change even if the VM is put in the stopped (deallocated) state. The address is only released when the NIC is deleted. You can change the assignment method after the NIC is created. Read the [Create a VM with a static public IP address](https://docs.microsoft.com/azure/virtual-network/virtual-network-deploy-static-pip-arm-portal) to learn more.
