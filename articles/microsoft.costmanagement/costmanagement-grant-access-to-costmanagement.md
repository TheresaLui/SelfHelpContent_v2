<properties
	pageTitle="How can I grant access to Cost Management?"
	description="grant access to cost management"
	service="microsoft.costmanagement"
	resource="costmanagement"
	authors="woodbridge"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b1d5b92d-4144-4fb4-a6b8-487fa4ac927d"
	ownershipId="ASMS_Billing"
/>

# How can I grant access to Cost Management?

Azure uses [Role-Based Access Control (RBAC)][1] to determine who can perform actions like creating and deleting budgets at different scopes (e.g. management groups, subscriptions, resource groups).

Grant access to Cost Management by adding users to the following roles for a given scope:

* Billing Reader
* Reader
* Contributor
* Owner

[Learn more about granting access](https://docs.microsoft.com/azure/role-based-access-control/quickstart-assign-role-user-portal)

## **Recommended documents**

* [Role-based access control](https://docs.microsoft.com/azure/role-based-access-control/)
* [Azure Cost Management ](https://docs.microsoft.com/azure/cost-management/)

[1]: https://docs.microsoft.com/azure/role-based-access-control/
