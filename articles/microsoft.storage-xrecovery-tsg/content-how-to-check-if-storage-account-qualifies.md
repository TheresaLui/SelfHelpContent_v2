<properties
	pageTitle="How to check if storage account type qualifies for recovery attempt from ASC"
	description="How to check if storage account type qualifies for recovery attempt from ASC"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="bf785128-c49e-4f87-a05f-432a59a8f13e"
/>

# How to check if storage account type qualifies for recovery

1. Navigate to Resource Explorer and search for the affected Storage Account resource.
2. In the Properties section, check the Type and ensure it is one of the following. No data recovery is possible for the types that do not qualify.
    1. Standard_GRS
	2. Standard_RAGRS
	3. Standard_GZRS
	4. Standard_RAGZRS
