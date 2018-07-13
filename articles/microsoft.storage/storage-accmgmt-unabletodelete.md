<properties
	pageTitle="Unable to delete Storage Account"
	description="Unable to delete Storage Account"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602694"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public,MoonCake"
/>

# Unable to delete Storage Account
Storage Account deletion is only possible if it does not contain any disk(s) that are attached to VM(s). Before deleting Storage Account, please ensure that:
1. [VM(s) with attached OS disk are deleted](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-2-delete-vm-to-detach-os-disk)
2. [Data disk(s) are detached from its VM(s)](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-3-detach-data-disk-from-the-vm)
