<properties
	pageTitle="Operation Failure RCA"
	description="RCA - VM marketplace purchase failure"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="OperationFailure_RCA-Marketplace-validation-failure"
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

To review and accept the legal terms, go to the Marketplace service in the Azure portal, or use PowerShell as described in [Accept the terms](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#accept-the-terms) in the article [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage). 




