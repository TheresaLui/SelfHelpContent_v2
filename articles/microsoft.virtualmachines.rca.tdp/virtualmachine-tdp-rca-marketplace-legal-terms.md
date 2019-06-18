<properties
	pageTitle="Operation Failure RCA"
	description="RCA - VM marketplace purchase failure"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="ValidationFailure_RCA-Marketplace-legal-terms"
	diagnosticScenario="OperationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# Your Azure Marketplace purchase needs your attention

<!--issueDescription-->
We detected a purchase failure for the deployment of Azure Marketplace offer **<!--$offerId-->offerId<!--/$offerId-->** using the subscription **<!--$subscriptionId-->subscriptionID<!--/$subscriptionId-->**. Your purchase cannot be completed until you accept the terms on the purchase offer.<br>
<!--/issueDescription-->

## Recommended Steps

You can browse images and current offers on [Azure Marketplace]( https://azuremarketplace.microsoft.com/) storefront and purchase them in the [Azure portal](https://azure.portal.com). You can also use the following commands:<br>

|Tool|Command|
|---|---|
| Azure PowerShell | [Get-AzMarketPlaceTerms](https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms)<br>[Set-AzMarketPlaceTerms](https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms) |
| Azure CLI | [az image show](https://docs.microsoft.com/en-us/cli/azure/image?view=azure-cli-latest#az-image-show)<br>[az vm image accept-terms](https://docs.microsoft.com/en-us/cli/azure/vm/image?view=azure-cli-latest#az-vm-image-accept-terms)|<br>

## Recommended Documents

- [Accept the terms](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#accept-the-terms).
- [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage)  
- [Find Linux VM images in the Azure Marketplace with the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage)
 







