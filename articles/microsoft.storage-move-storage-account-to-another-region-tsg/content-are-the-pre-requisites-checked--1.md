<properties
	pageTitle="Check for pre-requisite information"
	description="Check for pre-requisite information"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ca29c4a0-8b05-4ab1-b842-fa2074945ab2"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check for pre-requisite information

There is not a way to lift and move storage accounts from one region to another. To move a storage account, create a copy of your storage account in another region. Then, copy your data to that account by using AzCopy, or another tool of your choice. 

1. Ensure that the services and features that your account uses are supported in the target region. 
2. For preview features, ensure that your subscription is whitelisted for the target region. 
3. If you have active Azure VMs using Unmanaged disks you will need to stop/deallocate the VM. Once the copy is complete for all disks for a given VM, you would then be able to recreate the VM from this specialized OS VHD copy in the new region. 
