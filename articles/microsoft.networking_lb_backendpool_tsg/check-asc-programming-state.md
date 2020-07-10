<properties
	pageTitle="Check the network programming of a VM"
	description="Check the network programming of a VM"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="727ce48f-b78e-486b-b922-5e1b90a23cbe"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the network programming of a VM

## **Recommended Steps**

1. Select the VM with 'down DIPs' in ASC Resource Explorer
2. Go to "Properties" Tab > "Container Settings" Section
3. Ensure the following parameters have the expected values

	* IsNmProgrammingComplete = True<br>
	* IsNetworkAllocationComplete = True<br>
	* VscStateData = True

## **Recommended Documents**

* [Link to Wiki to check ASC for VM programming state](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265710/Azure_Virtual-Machine_CantRDPSSH_Basic-Workflow)
