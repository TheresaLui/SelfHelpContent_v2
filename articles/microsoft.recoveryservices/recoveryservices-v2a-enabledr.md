<properties
	pageTitle="Site Recovery (VMware to Azure)/Enable Protection"
	description="Site Recovery (VMware to Azure)/Common issues during Enable Protection"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536405"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Site Recovery (VMware to Azure)/Enable Protection

Common issues during Enable Replication**

## **Recommended Steps**

* Ensure you have used the capacity planning tool to avoid replication misses and not meeting the SLAs <add link>

* Ensure that the server that you are trying to protect meets the following requirements
-	Each disk should be less than 1TB in size
-	Number of disks should be less than x on regular storage and y on premium storage
-	The OS disk should be a basic disk and not dynamic disk
-	Name of the server should meet requirements of Azure virtual machine name – length should be less than 16 characters and contain Alphanumeric, underscore, and hyphen. For more details, see this http://aka.ms/asrstnaming
-	It is not UEFI enabled - http://aka.ms/asrstuefi

* Ensure that the server has the mobility service installed. If you choose to push install, the following requirements must be met
On the Windows Firewall of the machine you want to protect, select Allow an app or feature through Firewall. Enable File and Printer Sharing and Windows Management Instrumentation. For machines that belong to a domain you can configure the firewall settings with a GPO.

* Choose a valid storage account. Storage accounts of type RA-GRS and blob type are NOT supported.

* Ensure that the operating system meets the requirements.

* Ensure that the account credentials that are passed have administrator privilege to the machine.

## **Recommended  Documents**
[VMware to Azure](aka.ms/asrstv2a)
