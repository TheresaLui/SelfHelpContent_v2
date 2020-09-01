<properties
	pageTitle="Customer association issues"
	description="Customer association issues"
	infoBubbleText=""
	service="partnercenter"
	resource="PartnerCenter_Incentives"
	authors="Kim-Davis"
	ms.author="mallp"
	displayOrder=""
	articleId="incentives-customer-association-customer-association-issues"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739536"
	clientIds='partnercenter'
	resourceTags="PartnerCenter_Incentives"
	productPesIds="17005"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Incentives"
/>

# Partner Center Incentives: Customer association issues

## **Recommended Steps**
Below are some of the more common issues that you may encounter when submitting customer association (CPOR) claims:

**Sub-domain and Tenant Mismatch**

The CPOR association claim flow requires you to provide the customer tenant ID and subdomain. The customer tenant id and subdomain must match.  If you receive an error that they do not match, please reach out to the customer to ensure you have the correct details. 

**Subscription Errors in CPOR association claim flow**

In the CPOR association claim flow, you may be asked to provide a subscription for a product that you are trying to claim via Business Applications (Dynamics 365). The subscription is used to verify that the product and subscription belong to the tenant being claimed for and that the subscription is in active/in grace status. 

If you receive an error, it could be for several reasons:

1. The product selected doesn’t exist on the customer’s tenant
2. The subscription provided is not for Dynamics
3. The subscription provided is for CSP
4. The customer has not yet activated/provisioned the products for that subscription
5. The subscription has already been claimed
6. The identifier provided is not a subscription ID

**Next Step:** If you have a question regarding the accuracy of your subscription, please work with your customer to ensure the subscription is correct and that you are using the correct tenant ID. 
 

**Competing Claims Process and Timeline**

If you are creating a CPOR association claim for a customer and the product(s) has already been associated with another partner, your claim will go through arbitration:

1. After you create a new customer association, Microsoft will verify the details of the association and proof of execution provided to ensure its accuracy. 
2. If you and another partner claim for the same customer and product/workload, Microsoft will review each partner’s proof of execution documentation to determine which partner to approve. 
3. Additional information might be requested from both partners which could cause delays in processing your association request. 
4. Your CPOR association claim will still undergo its initial review within 5 business days.  The  status will remain Under Review while we work with the partner currently owning the product/workload.  You will be notified within the comments section of your claim if this is the case. 

**IMPORTANT:** If we require additional information to verify your CPOR association PoE, we’ll contact you via CPOR association claim comments section.

## **Recommended Documents**

* [Customer association issues](https://docs.microsoft.com/partner-center/incentives-customer-association-issues)
* [Manage customer associations](https://docs.microsoft.com/partner-center/incentives-manage-customer-associations)
* [Create a customer association using CPOR](https://docs.microsoft.com/partner-center/submit-osa-claim)
