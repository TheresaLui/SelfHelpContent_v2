<properties
	pageTitle="CSP Billing and Invoicing Reconciliation files"
	description="CSP Billing and Invoicing Reconciliation files"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="LauraBrenner"
	ms.author="labrenne"
	displayOrder=""
	articleId="partnercenter_reconciliation_files"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32692608"
	clientIds='partnercenter'
	resourceTags="csp"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Reconciliation files

## **Recommended Steps**

How is Effective unit price calculated for Azure plan consumption?
* Effective unit price is calculated at the meter level and recalculated daily based on consumption and tiering (if applicable). Refer to [Effective unit price calculation](https://docs.microsoft.com/partner-center/effective-unit-price-calculation)

What's the difference between billed and unbilled data?
* For one-time and recurring billing, the billing period is aligned to the full calendar month, and the invoice/reconciliation files will be available within the 6th and 8th of next month.
* Unbilled reconciliations are provided for partners who need to analyze the customer cost before the final invoice and reconciliation files are ready. Unbilled usage data is only an indicator of your estimates and should not be considered calculating billable invoice amount.

How to reconcile the Azure consumption in one-time purchase recon file?
* With the Azure subscription Id (Entitlement Id), you can obtain the Azure plan Id (Subscription Id) in the One-Time Purchase recon file. Search for this Id in the Daily-rated usage recon file to see all of the costs associated with this Azure plan Id, and the Azure Subscription Id is as Entitlement Id.

## **Recommended Documents**

* [Use the reconciliation files](https://docs.microsoft.com/partner-center/use-the-reconciliation-files)
* [Reconciliation file charge types](https://docs.microsoft.com/partner-center/recon-file-charge-types)
