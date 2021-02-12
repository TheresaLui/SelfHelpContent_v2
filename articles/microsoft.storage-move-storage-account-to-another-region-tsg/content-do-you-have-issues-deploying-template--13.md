<properties
	pageTitle="Deploy Template Using Azure portal"
	description="Deploy Template Using Azure portal"
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
	articleId="6f423dd6-ac39-4e1c-8558-ab7679f8c48f"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Deploy Template Using Azure portal

1. Deploy the template to create a new storage account in the target region. 
2. Save the template.json file. 
3. Enter or select the property values: Subscription, resource group, location. 
4. Click the I agree to the terms and conditions stated above checkbox, and then click the Select Purchase button. 

~~~powershell 

Get-AzSubscription 

$resourceGroupName = Read-Host -Prompt 'Enter the Resource Group name'

$location = Read-Host -Prompt 'Enter the location (i.e. centralus)' 

New-AzResourceGroup -Name $resourceGroupName -Location '$location' 

New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateUri '<name of your local template file>' 

~~~