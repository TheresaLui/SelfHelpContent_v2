<properties
	pageTitle="Site Recovery (Hyper-V Site to Azure)/Enable Protection"
	description="Site Recovery (Hyper-V Site to Azure)/Common issues during Enable Protection"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Site Recovery (Hyper-V Site to Azure)/Enable Protection

Common issues during Enable Replication**

## Recommended Steps

* Ensure you have used the capacity planning tool to avoid replication misses and not meeting the SLAs

* Ensure that the server that you are trying to protect meets the following requirements
-	Each disk should be less than 1TB in size
-	The OS disk should be a basic disk and not dynamic disk
-	Name of the server should meet requirements of Azure virtual machine name � length should be less than 16 characters and contain Alphanumeric, underscore, and hyphen. For more details, see this http://aka.ms/asrstnaming

* For generation 2/UEFI enabled virtual machines, the operating system family should be Windows and boot disk should be less than 300GB

* Choose a valid storage account. Storage accounts of type RA-GRS and blob type are NOT supported.

* Hyper-V servers should have fixes mentioned in article 2961977 installed. https://support.microsoft.com/kb/2961977

## Recommended  Documents
[Hyper-V Site to Azure](http://aka.ms/asrstb2a)