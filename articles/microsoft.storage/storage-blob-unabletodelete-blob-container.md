<properties
	pageTitle="Unable to delete Blob or Container"
	description="Unable to delete Blob or Container"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602738"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public,MoonCake"
/>

# Unable to delete Blob or Container
## **Recommended steps**
Storage Blob or Container deletion is **NOT** possible if is leased. Before deleting Blob or Container, please ensure that:

1. [VM(s) with attached OS disk are deleted](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-2-delete-vm-to-detach-os-disk) 
2. [Data disk(s) are not attached to a VM](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-3-detach-data-disk-from-the-vm)<br> 
3. There is no [lease on Blob](https://docs.microsoft.com/rest/api/storageservices/Lease-Blob?redirectedfrom=MSDN) or Container<br>
