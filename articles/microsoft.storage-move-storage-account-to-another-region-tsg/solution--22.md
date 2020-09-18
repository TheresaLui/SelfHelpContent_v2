<properties
	pageTitle="Discard or clean up"
	description="Discard or clean up"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6ada0f46-3471-483d-9419-db4815a46e5e"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Discard or clean up

<!--issueDescription-->

After the deployment, if you want to start over, you can delete the target storage account, and repeat the steps described in the Prepare and Move sections of this article. To commit the changes and complete the move of a storage account, delete the source storage account. 

**To remove a storage account by using the Azure portal:**

1. In the Azure portal, expand the menu on the left side to open the menu of services, and choose Storage accounts to display the list of your storage accounts. 
2. Locate the target storage account to delete, and right-click the More button (...) on the right side of the listing. 
3. select Delete, and confirm. 

**To remove the resource group and its associated resources, including the new storage account, use the Remove-AzStorageAccount command:**

~~~powershell

Remove-AzStorageAccount -ResourceGroupName  $resourceGroup -AccountName $storageAccount 

~~~

<!--/issueDescription-->

