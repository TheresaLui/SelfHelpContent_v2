<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM marketplace purchase failure - unavailable for subscription"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-Marketplace-unavailable-for-subscription"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# Your Azure Marketplace purchase needs your attention

<!--issueDescription-->
We detected a purchase failure for the deployment of Azure Marketplace offer **<!--$offerId-->offerId<!--/$offerId-->** using the subscription **<!--$subscriptionId-->subscriptionID<!--/$subscriptionId-->**. The offer you intended to purchase is not supported by the terms of your subscription.<br>
<!--/issueDescription-->

## Recommended Steps

- Go to the [Azure Marketplace]( https://azuremarketplace.microsoft.com/) storefront, or the Marketplace service in the [Azure portal](https://portal.azure.com), and cancel the offer.
- Select an offer that is supported by your subscription.<br>

## Recommended Documents

- [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage)  
- [Find Linux VM images in the Azure Marketplace with the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage)
- [Marketplace FAQs](https://docs.microsoft.com/azure/marketplace/marketplace-faq-publisher-guide)

 