
<properties
	pageTitle="Troubleshoot and resolve Azure Storage Firewall & VNet issues"
	description="Troubleshoot and resolve Azure Storage Firewall & VNet issues"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32682429,32682434,32682439,32682444"
	productPesIds="15629,16459,16461,16462,16598"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="2e1253fe-1a0a-4e87-98fb-757e7b33df75"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot and resolve Azure Storage Firewall & Virtual Network issues 

## **Recommended Steps**

Most customers resolved their firewall & virtual network related connectivity failure issues, from other Azure Services, using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions. 

### **Trusted Microsoft services is added to the exception still storage connections get blocked**
 
Only a subset of Microsoft Azure services are part of the [**Trusted Microsoft services** list](https://docs.microsoft.com/azure/storage/common/storage-network-security#trusted-microsoft-services). Any service not on the list wouldn't work until the public IP or VNet of that service is explicitly added to the exception list. Refer below to know how to resolve the issue for the most commonly reported services. 

### **Azure service getting blocked is in a different region than storage account**

If the service getting blocked is in a different region than storage account, then the public IP of the Azure service needs to be added to the Firewall. Some services might have a set of outbound IP addresses or range of address and in that case the whole list or range needs to be added. Please refer to the documentation for the service to find the public IP. Once you have the public IP add it to the storage account settings by referring to this [article](https://docs.microsoft.com/azure/storage/common/storage-network-security#grant-access-from-an-internet-ip-range). Alternately, you can navigate back and open a support case by selecting the corresponding product and get help in getting the public IP for the service.    

### **Azure service getting blocked is in the same region as storage account**
 
In the case where the Azure service is in the same region as the storage account, communication happens within the intranet. The IP address used by the service to communicate to storage is an internal (private) IP and hence the virtual network associated with the service needs to be added mandatorily. Adding the public IP of the service to the Firewall address range wouldn't unblock the traffic. Adding the private IP of the service to the Firewall address range might unblock the traffic but will get blocked if the address changes and hence is unreliable.

Below is the list of some commonly reported services and steps to add virtual network for them. If you require help adding virtual network to the service, you can navigate back and open a support case by selecting the corresponding product. Once the virtual network is associated with the service add it to the storage account settings by referring to this [article](https://docs.microsoft.com/azure/storage/common/storage-network-security#managing-virtual-network-rules).

* **Web & Mobile**: [Web App](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet)
* **Compute Services**: 
	
	* [Function App](https://docs.microsoft.com/azure/azure-functions/functions-create-vnet#connect-your-function-app-to-your-vnet)
	* [Kubernetes Services](https://docs.microsoft.com/azure/aks/concepts-network#azure-virtual-networks)
	* [OpenShift Container](https://docs.openshift.com/container-platform/3.10/install_config/configuring_azure.html#configuring-azure-objects_configuring-for-azure)
	
* **Networking**: [ExpressRoute](https://docs.microsoft.com/azure/architecture/reference-architectures/hybrid-networking/expressroute#architecture) - Every ExpressRoute circuit is given two IP addresses at the Microsoft Edge that are used to connect to Microsoft Services like Azure Storage. To allow communication from your circuit to Azure Storage you must configure the storage account's 'Firewall and virtual networks' configuration to add those two IP addresses on your storage account. Please open a support case under Networking to get the two IPs. 	 
* **Databases**: [SQL DB Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-vnet-subnet)
* **Monitoring and Management**: [Azure Automation](https://docs.microsoft.com/azure/automation/automation-hybrid-runbook-worker)	
* **Intelligence and Analytics**: [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-blob-storage#supported-capabilities)
