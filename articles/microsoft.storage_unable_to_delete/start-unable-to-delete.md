<properties
	pageTitle="Unable to delete workflow"
	description="Unable to delete workflow"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32602738"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7cdec46d-9d0c-4a41-a52a-3b221355105f"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Unable to delete workflow

1. This workflow provides steps to assist customers with problems deleting VHDs, images, and storage accounts from their subscription.
2. For example:
   1. The customer is unable to delete a VHD (page blob). Usually, this is because there is still a lease on the VHD.
   2. The customer is unable to delete a Storage Account. Usually, this is because there are still leased VHDs or VM images residing in their Storage Account.
   3. The customer is unable to delete a VM Image. Usually, this is because they cannot locate the image.
3. In order to start this TSG, some preliminary information is required. 
4. If this information has not been provided, then we will help with steps to find possible error messages. 
