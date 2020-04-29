<properties
	pageTitle="Problems with scoping filters"
	description="Problems with scoping filters"
	infoBubbleText="Problems with scoping filters"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629803"
	productPesIds="16666"
	articleId="8d591007-b406-4b63-9f3e-451f17322ef4"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with scoping filters

## **Recommended Steps**

**Workday to AD User Provisioning does not set manager attribute value for AD user account**

The Workday to AD User Provisioning job is not setting manager attribute value for AD user accounts. There are two possible scenarios when this behavior is seen:

1. The manager in Workday cannot be resolved to a corresponding AD User account because the manager is not in scope
1. In a multiple AD domains scenario, the manager in Workday is not present in the same domain as the user

Try these steps to resolve the issue:

1. If you have defined scoping filters, first check if the manager is in scope and it satisfies the scoping clause. If the manager does not satisfy the scoping filter, change the filter so that the manager is also in scope of the provisioning operation.
1. If you have multiple AD domains, then the connector has a known limitation of unable to resolve cross-domain manager references

## **Recommended Documents**

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
