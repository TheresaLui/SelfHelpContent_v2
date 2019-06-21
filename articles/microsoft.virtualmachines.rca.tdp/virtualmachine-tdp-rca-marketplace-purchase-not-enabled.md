<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM marketplace purchase failure - payment not enabled"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-Marketplace-purchase-not-enabled"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# Your Azure Marketplace purchase needs your attention

<!--issueDescription-->
We detected a purchase failure for the deployment of Azure Marketplace offer **<!--$offerId-->offerId<!--/$offerId-->** using the subscription **<!--$subscriptionId-->subscriptionID<!--/$subscriptionId-->**.<br> 
<!--/issueDescription-->

Your purchase cannot be completed until the offer is enabled for purchase.<br>

## Recommended Steps

The enrollment administrator controls privileges on which accounts can make the purchase. Contact the publisher or your system administrator to acertain the needed requirements.

## Recommended Documents

- [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage)  
- [Find Linux VM images in the Azure Marketplace with the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage)
- [Marketplace FAQs](https://docs.microsoft.com/azure/marketplace/marketplace-faq-publisher-guide)

 
