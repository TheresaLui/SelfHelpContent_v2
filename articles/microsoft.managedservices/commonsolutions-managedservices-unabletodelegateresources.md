<properties
	pageTitle="Unable to delegate resources"
	description="Unable to delegate resources"
	infoBubbleText="Unable to delegate resources"
	service="microsoft.managedservices"
	resource="managedservices"
	authors="prukulka"
	ms.author="prukulka"
	displayOrder=""
	articleId="CommonSolutions-managedservices-unabletodelegateresources"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32642169"
	resourceTags=""
	productPesIds="16761"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_AzureLighthouse"
/>

# Unable to delegate resources

Most users are able to delegate resources using the steps below.

## **Recommended Steps**

**Can't delegate resources to a service provider?**

- Delegation must be done by a non-guest account in the customer's tenant which has the Owner built-in role for the subscription being onboarded (or which contains the resource groups that are being onboarded)
  - To see all users who can delegate the subscription, a user in the customer's tenant can select the subscription in the Azure portal, open Access control (IAM), and view all users with the Owner role

## **Recommended Documents**

* [Delegate resources](https://docs.microsoft.com/azure/lighthouse/how-to/view-manage-service-providers#delegate-resources)
* [List owners of a subscription](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-list-portal#list-owners-of-a-subscription)
