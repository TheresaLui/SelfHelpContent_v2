<properties
	pageTitle="Unable to delete Blob or Container"
	description="Unable to delete Blob or Container"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602738"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="867e9c97-2a7b-43c4-9ae3-be0d5181e5d5"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to delete Blob or Container
## **Recommended steps**
Follow steps below and retry Blob or Container deletion:

1. [Delete any OS disk(s)](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-2-delete-vm-to-detach-os-disk) in the Blob or Container<br>
2. [Detach any data disk(s)](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-3-detach-data-disk-from-the-vm) in the Blob or Container<br> 
3. Break any [Blob](https://docs.microsoft.com/rest/api/storageservices/Lease-Blob?redirectedfrom=MSDN) or [Container lease](https://docs.microsoft.com/rest/api/storageservices/lease-container)<br>
