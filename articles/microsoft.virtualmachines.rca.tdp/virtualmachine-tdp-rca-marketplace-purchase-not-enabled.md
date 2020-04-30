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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# Your Azure Marketplace purchase needs your attention

<!--issueDescription-->
We detected a purchase failure for the deployment of Azure Marketplace offer **<!--$offerId-->offerId<!--/$offerId-->** using the subscription **<!--$subscriptionId-->subscriptionID<!--/$subscriptionId-->**.<br> 
<!--/issueDescription-->

Your purchase cannot be completed until the offer is enabled for purchase.<br>

## **Recommended Steps**

If your subscription was converted from the Pay-as-You-Go environment to Azure Enterprise Agreement, Azure Marketplace services are not converted. In order to have a single view of all subscriptions and charges, we recommend you add the Azure Marketplace services to the Azure Enterprise portal.<br>

1. Sign in to the [Microsoft Azure Enterprise Portal](https://ea.azure.com/)
1. Select **Manage** on the left navigation
1. Select the **EnrollmentTab**
1. View the **Enrollment Detail** section
1. To the right of the Azure Marketplace field, select the pencil icon to enable it. Select **Save**.

The account owner can now purchase any Azure Marketplace services that were previously owned in the Pay-As-You-Go subscription.<br>

After the new Azure Marketplace subscriptions are activated under your Azure EA enrollment, cancel the Azure Marketplace services that were created in the Pay-As-You-Go environment. This step is critical so that your Azure Marketplace subscriptions do not fall into a bad state when your Pay-As-You-Go payment instrument expires.<br>

**If you have an Azure Enterprise account**, you can enable the purchase directly in the [Microsoft Azure Enterprise Portal](https://ea.azure.com/).

## **Recommended Documents**

- [Get started with the Azure Enterprise portal](https://docs.microsoft.com/azure/cost-management-billing/manage/ea-portal-get-started)<br>
- [Find Windows VM images in the Azure Marketplace with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage)<br>
- [Find Linux VM images in the Azure Marketplace with the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage)<br>
- [Marketplace FAQs](https://docs.microsoft.com/azure/marketplace/marketplace-faq-publisher-guide)
