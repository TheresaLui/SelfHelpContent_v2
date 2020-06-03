<properties
	pageTitle="Confirm if VM is a managed VM "
	description="Confirm if VM is a managed VM"
	service=""
	resource=""
	authors="TestAuthor"
	ms.author="TestAuthor"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="59a6a63a-ef40-408b-9481-cf296f8da475"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if it is a managed VM

1. Go to ASC-> Resource Explorer -> Select the VM
2. Confirm you have a field called "Managed disk"  pointig to a Managed OS disk
3. If VM does not have that field and has a property called "OS disk Storage Account name", then VM is unmanaged
