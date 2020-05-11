<properties
	pageTitle="Blob Active Lease"
	description="Blob Active Lease"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b45b90d8-fecb-4c9a-b48d-547865386ede"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Blob Active Lease
<!--issueDescription-->
We've researched your case and believe the issue is due to a lease existing on the blob. This commonly happens when VM images and disks are still attached to an Azure VM. In this scenario, the VM will hold a lease on a blob, preventing deletion.
<!--/issueDescription-->

## **Recommended Steps**

1. Open the Ibiza Portal at https://portal.azure.com  
2. On the left-hand navigation pane, click on "Disks (classic)", "OS images (classic)", or "VM images (classic)"
a. If you do not see either of these options, click on "More services >" in the lower left, and locate these options in the resulting search blade
3. You will be presented with a list of all the Classic Disks, Classic VM Images or Classic OS Images that are present in the entire subscription. There are two important pieces of information that you may need: 
	1. "State" indicates whether the OS Disk is currently attached to a VM
	2. For Classic Disks and OS Images you should see the properties Attached To: VM where the Disk is attached to (if any), Storage Account, Media Link: Full path to the Blob location
4. For Classic VM Images, after browsing the resource you will see all the Classic Disks(OS and Data) associated to it
a. For the Disks resources associated with the VM Image you can Right Click and select "View Media Link" to see the full path to the Blob location as well as the Storage Account
5. To release the lease of all these objects (Classic Disks and Images) customer may select the desired resource/s and proceed to the "Delete" button. Note: The lease will be released and Storage Account deletion and Blob deletion operations should be unblocked.

## **Recommended Documents**

1. [https://docs.microsoft.com/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors)
2. [Troubleshoot classic storage resource deletion errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/storage-classic-cannot-delete-storage-account-container-vhd)
