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
	cloudEnvironments="public"
	articleId="727ce48f-b78e-486b-b922-5e1b90a23cbe"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the network programming of a VM

## **Recommended Steps**

* Select the VM with 'down DIPs' in ASC Resource Explorer
* Go to Properties > Container Settings and check to ensure IsNmProgrammingComplete = True and IsNetworkAllocationComplete = True and VscStateDate = True
  
## **Recommended Documents**

* [Link to Wiki to check ASC for VM programming state](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/CantRDPSSH/Basic_Workflow)
