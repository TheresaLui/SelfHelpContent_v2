<properties
	pageTitle="Check if VM is a managed VM"
	description="Check if VM is a managed VM"
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
	articleId="aefa7b36-5b59-4361-aaa6-d99a6125829f"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if it is a managed VM

1. Go to ASC-> Resource Explorer -> Select the VM
2. Confirm you have a field called "Managed disk"  pointig to a Managed OS disk
3. If VM does not have that field and has a property called "OS disk Storage Account name", then VM is unmanaged
