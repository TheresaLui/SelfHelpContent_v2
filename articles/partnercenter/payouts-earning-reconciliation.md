<properties
	pageTitle="Payouts - Earning reconciliation issues"
	description="SelfHelp for Payouts Product - Earning reconciliation issues"
	infoBubbleText=""
	service="partnercenter"
	resource="isv"
	authors="A-COFLOR"
	ms.author="A-COFLOR"
	displayOrder=""
	articleId="partnercenter_payouts_earning_reconciliation"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32750766" 
	clientIds='partnercenter'
	resourceTags="isv"
	productPesIds="17010"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Payouts"
/>
# Earning reconciliation issues

## **Recommended Steps**

**How do I reconcile payout statements to order or usage reports in analytics?**

You can use AssetID, orderID and line item ID appearing in payout transaction history report with analytic orders and usage reports. See below for mapping.
* Payout Transaction History.AssetID = order.OrderID
* Payout Transaction History.OrderID & LineItem = Usage.UsageReferenceID [OrderID:LineItemID]

**How do I know when to expect payments for my customer orders?**

* First, using your assetID, check customer orders in [Orders reports](https://partner.microsoft.com/dashboard/commercial-marketplace/analytics/order)
* Check customer channel for your customer subscription in [customers report](https://partner.microsoft.com/dashboard/commercial-marketplace/analytics/customer)
* For enterprise customers, publisher earnings appear in the statement 1-2 days after the Purchase Order date
* For non-enterprise customers, publisher earnings appears in the statement 1-2 days after customer payment is received

## **Recommended Documents**

* [Payout Summary Overview](https://docs.microsoft.com/azure/marketplace/partner-center-portal/payout-summary-overview)
* [Orders dashboard in commercial marketplace analytics](https://docs.microsoft.com/azure/marketplace/partner-center-portal/orders-dashboard)
