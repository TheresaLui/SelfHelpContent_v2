<properties
	pageTitle="Cannot manage projected resources"
	description="Cannot manage projected resources"
	infoBubbleText="Cannot manage projected resources"
	service="microsoft.managedservices"
	resource="managedservices"
	authors="prukulka"
	ms.author="prukulka"
	displayOrder=""
	articleId="CommonSolutions-managedservices-cannotmanageprojectedresources"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32642165"
	resourceTags=""
	productPesIds="16761"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_AzureLighthouse"
/>

# Cannot manage projected resources

Most users are able to manage projected resources using the steps below.

## **Recommended Steps**

**Can't remove a customer delegation?**

There are two ways to remove a delegation:

- In order to remove a delegation, the Managed Services Registration Assignment Delete Role must have been assigned when onboarding the customer. Users with this role can remove a delegation. 
-  Customers can remove delegation from their tenant. Remember: Delegation must be done by a non-guest account in the customer's tenant which has the Owner built-in role for the subscription being onboarded.

**Can't deploy policy to customers?**

- As a service provider, you may have onboarded multiple customer tenants for Azure delegated resource management. Azure Lighthouse allows service providers to perform operations at scale across several tenants at once, making management tasks more efficient. [This](https://docs.microsoft.com/azure/lighthouse/how-to/policy-at-scale) topic shows you how to use Azure Policy to deploy a policy definition and policy assignment across multiple tenants using PowerShell commands.

## **Recommended Documents**

* [Remove access to a delegation](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#remove-access-to-a-delegation)
* [How to deploy policy at scale](https://docs.microsoft.com/azure/lighthouse/how-to/policy-at-scale)
