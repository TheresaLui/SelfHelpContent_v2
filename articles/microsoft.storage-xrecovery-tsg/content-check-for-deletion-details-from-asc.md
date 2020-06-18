<properties
	pageTitle="How to check for deletion details from ASC"
	description="How to check for deletion details from ASC"
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
	articleId="deaa5095-2c36-4dc2-bfc1-1fadcc47a67c"
/>

# How to check for deletion details from ASC

1. Navigate to **Resource Explorer** and search for the affected Storage Account resource.
2. Select **Blob** tab/section.
3. Navigate to the subsection **Blob/Container Deletion Lookup & Recovery**
4. Click + **Get Deletion & Recovery Info** and fill the details of the deletion operation of the resource we are attempting to recover and **Run** the query.
5. Once status is **Succeeded**, review the Result and Recover Status
