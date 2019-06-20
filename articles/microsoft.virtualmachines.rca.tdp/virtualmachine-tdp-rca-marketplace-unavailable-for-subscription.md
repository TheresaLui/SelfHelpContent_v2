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
We detected a purchase failure for the deployment of Azure Marketplace offer **<!--$offerId-->offerId<!--/$offerId-->** using the subscription **<!--$subscriptionId-->subscriptionID<!--/$subscriptionId-->**. <br>
<!--/issueDescription-->

The offer you intended to purchase is available for your subscription or location.<br>

## Recommended Steps

If this offer has been created recently, please allow up to 30 minutes for this offer to be available for purchase. 

If still unavailable, go to the [Azure Marketplace](https://azuremarketplace.microsoft.com/) or the Marketplace service in the [Azure Portal](https://portal.azure.com/) to select an image that is supported by your subscription and location. You can also use PowerShell and the Azure CLI:

- For PowerShell examples, see [Navigate the images](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/cli-ps-findimage#navigate-the-images).
- For Azure CLI examples, see [List popular images](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage#list-popular-images).

## Recommended Documents

- [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage)  
- [Find Linux VM images in the Azure Marketplace with the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage)
- [Marketplace FAQs](https://docs.microsoft.com/azure/marketplace/marketplace-faq-publisher-guide)

 