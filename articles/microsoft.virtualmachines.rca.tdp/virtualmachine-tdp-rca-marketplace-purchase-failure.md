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
We detected that your Azure Marketplace purchase of the offer **<!--$offerId-->item<!--/$offierId-->** cannot be completed because the legal terms for this transaction have not been accepted for using with the **<!--$subscriptionId-->subscriptionID<!--/$subscriptionId-->** subscription.<br>
<!--/issueDescription-->

Your purchase cannot be completed until you accept legal terms on the purcahse offer. 

To review and accept the legal terms, go to the Marketplace service in the Azure portal, or use PowerShell as described in [Accept the terms](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#accept-the-terms) in the article [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage). 




