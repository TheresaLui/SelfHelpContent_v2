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

The offer you intended to purchase is currently unavailable.<br>

## Recommended Steps

When you select an offer, the possibility exists that not all of the data that determines purchase availability is known at the time. The purchase terms in accordance with your subscription are subject to change by the publisher. If still unavailable, contact the publisher for recommendations or you can determine which images are available in your region by using PowerShell and the Azure CLI. 

- For PowerShell examples, see [Navigate the images](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#navigate-the-images).
- For Azure CLI examples, see [List popular images](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage#list-popular-images).

## Recommended Documents

- [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage)  
- [Find Linux VM images in the Azure Marketplace with the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage)
- [Marketplace FAQs](https://docs.microsoft.com/azure/marketplace/marketplace-faq-publisher-guide)

 