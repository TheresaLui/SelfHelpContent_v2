<properties
	pageTitle="Billing and Invoicing Reconciliation file Reseller MPNID missing or incorrect"
	description="Billing and Invoicing Reconciliation file Reseller MPNID missing or incorrect"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="LingnaXu"
	ms.author="v-linx"
	displayOrder=""
    articleId="partnercenter_billing_and_invoicing_reconciliation_file_reseller_mpnid_missing_or_incorrect"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32781873" 
	clientIds='partnercenter'
	resourceTags="csp"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>

# Billing and Invoicing Reconciliation file Reseller MPNID missing or incorrect

## **Recommended Steps**

* If a CSP partner sold the subscription directly to the customer, their MPN ID is listed under MPN ID. The Reseller MPN ID will be 0 since no reseller was involved in the purchase.
* If a reseller has purchased the product for a customer, the Reseller MPN ID will be populated in the reconciliation file. However, the reseller must have an active MPN ID at the time of the purchase, and it must be linked with the partner.
* If the CSP partner removes a Reseller MPN ID, this value will be set to -1.
* If you need to update a Reseller MPN ID, see [Reseller MPN ID](https://docs.microsoft.com/partner-center/use-the-reconciliation-files#reseller-mpn-id).

## **Recommended Documents**

* [Use the reconciliation files](https://docs.microsoft.com/partner-center/use-the-reconciliation-files)
* [Use the reconciliation files as developer](https://docs.microsoft.com/partner-center/develop/invoice-resources)