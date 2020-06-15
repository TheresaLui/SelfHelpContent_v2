<properties
	pageTitle="Export a template "
	description="Export a template "
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
	articleId="74676ef9-6e7d-4ba4-b021-f433fefec8a8"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Export a template 

This template contains settings that describe your storage account. To export a template by using Azure portal: 

1. Sign in to Azure portal 
2. Select your storage account 
3. select > settings > Export template 
4. Choose Download in the Export template blade. 
5. Locate the .zip file that you downloaded from the portal, and unzip that file to a folder of your choice.This zip file contains the .json files that comprise the template and scripts to deploy the template. 
6. Export by PowerShell: 

~~~powershell

Connect-AzAccount 

$context = Get-AzSubscription -SubscriptionId <subscription-id> 

Set-AzContext $context 

$resource = Get-AzResource -ResourceGroupName <resource-group-name>  -ResourceName <storage-account-name>  -ResourceType Microsoft.Storage/storageAccounts 

Export-AzResourceGroup -ResourceGroupName <resource-group-name> -Resource $resource.ResourceId 

~~~