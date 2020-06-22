<properties
	pageTitle="Ensure source account has no disks attached to VM"
	description="Ensure source account has no disks attached to VM"
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
	articleId="4d19b0f6-05d4-48d5-b6c6-50b5ec3789e6"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Ensure source account has no disks attached to VM

Source storage accounts could have disks which are attached to a virtual machine. We need to ensure that the VMs to be stop/deallocated before we start the move. 

To check if there are any disks use ASC to determine.

1. Open [ASC](https://azuresupportcenter.msftcloudes.com/caseoverview) and check the storage account for any attached disks. (***Storage Account -> VHD tab***). Results show the VM attached. 
2. If you have active Azure VMs using Unmanaged disks you will need to ask Cx stop/deallocate the VM. Once the move is complete for all disks for a given VM, you would then be able to recreate the VM from this specialized OS VHD copy in the new region.  
