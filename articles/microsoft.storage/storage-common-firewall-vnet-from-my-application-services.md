
<properties
	pageTitle="Troubleshoot and resolve Azure Storage Firewall & VNet issues"
	description="Troubleshoot and resolve Azure Storage Firewall & VNet issues"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32682428,32682433,32682438,32682443"
	resourceTags=""
	productPesIds="15629,16459,16461,16462,16598"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="738c563d-2440-4919-bb3e-fd76192ea87b"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot and resolve Azure Storage Firewall & Virtual Network issues 

Most customers resolved their firewall & virtual network related connectivity failure issues, from their own applications, using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions. 

Own applications cover anything deployed on IaaS VMs, Cloud Service deployments, on another cloud or on premise. The application could be Storage Explorer, any storage tools or custom applications. 

_If the issue is from a Microsoft hosted service like Web Apps, Functions Apps, SQLDB , HDI etc please navigate one step back and choose the problem subtype as "Not able to connect from other Azure Service."_ 

## **Recommended Steps**

* Trusted Microsoft services is added to the exception still storage connections get blocked

	Only a subset of Microsoft Azure services is part of the [Trusted Microsoft services list](https://docs.microsoft.com/azure/storage/common/storage-network-security#trusted-microsoft-services). Any service not on the list wouldn't work until the public IP or VNet of that service is explicitly added to the exception list. Refer below to know how to resolve the issue for the most commonly reported services. 

* My application getting blocked is in a different region than storage account

	* If the application getting blocked is in a different region than storage account, then the public IP of the application needs to be added to the Firewall
	* If it's an application on an Azure VM it would be the [Public IP of the IaaS VM](https://docs.microsoft.com/azure/virtual-network/associate-public-ip-address-vm)
	* If it's Storage Explorer on your client machine then it's the Public IP which the request has which typically is an ISP or Proxy IP. You can use a browser and a site like [What's my Public IP](https://www.whatsmyip.org/) to find your public IP.
	* Some services might have a set of outbound IP addresses or range of address and in that case the whole list or range needs to be added. Please refer to the documentation for the service to find the public IP. Once you have the public IP add it to the storage account settings by referring this [article](https://docs.microsoft.com/azure/storage/common/storage-network-security#grant-access-from-an-internet-ip-range). Alternately, you can navigate back and open a support case by selecting the corresponding product and get help in getting the public IP for the service.
	* [Connecting over ExpressRoute](https://docs.microsoft.com/azure/architecture/reference-architectures/hybrid-networking/expressroute#architecture) - Every ExpressRoute circuit is given two IP addresses at the Microsoft Edge that are used to connect to Microsoft Services like Azure Storage. To allow communication from your circuit to Azure Storage you must configure the storage account's 'Firewall and virtual networks' configuration to add those two IP addresses on your storage account. Please open a support case under Networking to get the two IPs.

* Application getting blocked is in the same region as storage account
 
 	In the case where your application is in the same Azure region as the storage account, communication happens within the intranet. The IP address used, say by the IaaS VM to communicate to storage is an internal (private) IP and hence the virtual network associated with the service needs to be added mandatorily. Adding the public IP of the IaaS VM to the Firewall address range wouldn't unblock the traffic. Adding the private IP of the service to the Firewall address range might unblock the traffic but will get blocked if the address changes and hence is unreliable.

* Application on IaaS Virtual Machines 
  
  * Application on an ARM IaaS VM - ARM VMs can't be deployed without a virtual network. So, if an ARM IaaS is deployed it already has a VNet, refer for details [Virtual machines and virtual network in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/network-overview). You need to add this virtual network to the Storage Firewall by following [Grant firewall access from a virtual network](https://docs.microsoft.com/azure/storage/common/storage-network-security#grant-access-from-a-virtual-network).
  * Application on a Classic IaaS VM - Classic VMs support classic VNets only and  storage firewall doesn't support classic VNets. Enabling firewall on the storage firewall can impact your applications ability to connect to storage. General recommendation is to migrate the Classic VMs to ARM deployed VMs. In the interim you might need to disable the storage firewall.

* Application on Azure Cloud Services 

	* Azure Cloud Service only supports Classic deployment model today and the Vnet limitations are specified here [Azure Cloud Services can't be places in ARM virtual networks](https://docs.microsoft.com/azure/cloud-services/cloud-services-connectivity-and-networking-faq#how-can-i-use-azure-resource-manager-virtual-networks-with-cloud-services) 
