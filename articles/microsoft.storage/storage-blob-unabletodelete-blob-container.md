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
You might receive an error when you try to delete the Azure Storage Account, Container, or Blob. This issue may occur under the following circumstances:

- When you delete a VM, the disk and VHD are not automatically deleted. That might be the reason for deletion failure. We don’t delete the disk so that you can use the disk to mount another VM.<br>
- There is a lease on the object you are trying to delete<br>

If this Blob or Container was attached to a VM, follow steps in [troubleshoot Storage resource deletion errors](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors) to delete the object.

## **Recommended documents**
[Troubleshoot Storage resource deletion errors](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors)<br>
[Delete Storage Account operation](https://msdn.microsoft.com/library/azure/hh264517.aspx)<br>
[Delete Container operation](https://docs.microsoft.com/rest/api/storageservices/delete-container)<br>

