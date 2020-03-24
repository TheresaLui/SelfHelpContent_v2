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
	cloudEnvironments="public"
	articleId="7cdec46d-9d0c-4a41-a52a-3b221355105f"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Unable to delete workflow

* This workflow provides steps to assist customers with problems deleting VHDs, images, and storage accounts from their subscription.
* For example:
  * The customer is unable to delete a VHD (page blob). Usually, this is because there is still a lease on the VHD.
  * The customer is unable to delete a Storage Account. Usually, this is because there are still leased VHDs or VM images residing in their Storage Account.
  * The customer is unable to delete a VM Image. Usually, this is because they cannot locate the image.
* In order to start this TSG, some preliminary information is required. 
* If this information has not been provided, then we will help with steps to find possible error messages. 
