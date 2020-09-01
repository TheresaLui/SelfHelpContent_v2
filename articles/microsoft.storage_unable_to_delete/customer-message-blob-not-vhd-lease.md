<properties
	pageTitle="Blob(Not VHD) Active Lease"
	description="Blob(Not VHD) Active Lease"
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
	articleId="9045f904-36c6-4e0c-8245-71ca0bd8fd46"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>
# Blob(Not VHD) Active Lease
<!--issueDescription-->
We've researched your case and believe the issue is due to a lease existing on the blob. This lease, if not on a VHD, was something explicitly configured by you or someone in your organization for this resource. Leased blobs cannot be deleted without breaking the lease first. 
<!--/issueDescription-->

## **Recommended Steps**

To break the lease, please use the PowerShell commands listed in the documents below. 

## **Recommended Documents**

* [Break lease for ARM blobs](https://gallery.technet.microsoft.com/How-to-break-the-locked-d01ba283)
* [Break lease for classic blobs](https://gallery.technet.microsoft.com/How-to-break-the-locked-c2cd6492)
* [Command reference for lease release](https://docs.microsoft.com/cli/azure/storage/blob/lease?view=azure-cli-latest#az-storage-blob-lease-release)
* [Command reference for lease break](https://docs.microsoft.com/cli/azure/storage/blob/lease?view=azure-cli-latest#az-storage-blob-lease-break)
