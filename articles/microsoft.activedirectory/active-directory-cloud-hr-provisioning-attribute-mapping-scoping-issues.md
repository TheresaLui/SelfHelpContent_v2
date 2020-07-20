<properties
	pageTitle="Problem configuring attribute mappings or scoping filters"
	description="Problem configuring attribute mappings or scoping filters"
	infoBubbleText="Problem configuring attribute mappings or scoping filters"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684513"
	productPesIds="16666"
	articleId="42641575-7bcf-45f9-8234-9d34cdb35d07"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problem configuring attribute mappings or scoping filters

## **Recommended Steps**

**Issue with conflicting UPN values**

The Workday to AD User Provisioning Workday to AD User Provisioning shows error message "HybridSynchronizationActiveDirectoryUserPrincipalNameNotUnique". The operation failed because UPN value provided for addition/modification is not unique forest-wide. Error Details: CONSTRAINT_ATT_TYPE - userPrincipalName.

The "userPrincipalName" value that Workday connector is trying to set when creating the AD user account already exists in the target AD domain. This implies that either (1) the user already exists and the matching ID check failed for the user or (2) the UPN generation rule generated a conflicting value.

Here are the suggested resolution steps:

1. If the user already exists and the matching ID check failed to link the Workday account to Active Directory account, then check if the matching ID attribute (typically: employeeID) in both Workday and AD have an exact match. If they don't have a match, it is a data issue that needs to be fixed. For e.g. if the EmployeeID in Workday is 001052 and in AD it is 1052, then the provisioning engine will fail to link the two accounts and try to create a user that already exists. The solution in this case is to change the EmployeeID value in AD to include the leading zeros to make it 001052.
1. If the UPN generating expression is not generating a unique value, consider using the de-duplication function **[SelectUniqueValue](https://docs.microsoft.com/azure/active-directory/manage-apps/functions-for-customizing-application-data#selectuniquevalue)** to generate a unique value each time

**Workday to AD User Provisioning does not set manager attribute value for AD user account**

The Workday to AD User Provisioning job is not setting manager attribute value for AD user accounts. There are two possible scenarios when this behavior is seen:

1. The manager in Workday cannot be resolved to a corresponding AD User account because the manager is not in scope
1. In a multiple AD domains scenario, the manager in Workday is not present in the same domain as the user

Try these steps to resolve the issue:

1. If you have defined scoping filters, first check if the manager is in scope and it satisfies the scoping clause. If the manager does not satisfy the scoping filter, change the filter so that the manager is also in scope of the provisioning operation.
1. If you have multiple AD domains, then the connector has a known limitation of unable to resolve cross-domain manager references

## **Recommended Documents**

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
