<properties
	pageTitle="Operation Failure RCA"
	description="RCA - VM marketplace purchase failure"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-Marketplace-legal"
	diagnosticScenario="OperationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# Your Azure Marketplace purchase needs your attention

<!--issueDescription-->
We detected a purchase failure for the deployment of Azure Marketplace offer **<!--$offerId-->offerId<!--/$offerId-->** using the subscription **<!--$subscriptionId-->subscriptionID<!--/$subscriptionId-->**.<br>
<!--/issueDescription-->

 Your purchase cannot be completed until you accept the terms on the purchase offer.<br>

## Recommended Steps

In the [Azure portal](https://portal.azure.com), accept the terms of the offer in the Marketplace service. You can also use Azure PowerShell or Azure CLI:

- For PowerShell, use the [Get-AzMarketPlaceTerms](https://docs.microsoft.com/powershell/module/az.marketplaceordering/get-azmarketplaceterms) and [Set-AzMarketPlaceTerms](https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms) commands. For an example, see [Accept the terms](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#accept-the-terms).
- For Azure CLI, use the [az image show](https://docs.microsoft.com/cli/azure/image?view=azure-cli-latest#az-image-show) and [az vm image accept-terms](https://docs.microsoft.com/cli/azure/vm/image?view=azure-cli-latest#az-vm-image-accept-terms) commands. For an example, see [Accept the terms](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage#accept-the-terms).<br>

## Recommended Documents

- [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage)  
- [Find Linux VM images in the Azure Marketplace with the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage)
- [Marketplace FAQs](https://docs.microsoft.com/azure/marketplace/marketplace-faq-publisher-guide)
