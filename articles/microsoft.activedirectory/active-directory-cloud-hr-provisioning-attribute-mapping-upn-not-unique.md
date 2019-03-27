<properties
	pageTitle="Workday to AD User Provisioning shows error message HybridSynchronizationActiveDirectoryUserPrincipalNameNotUnique"
	description="Workday to AD User Provisioning shows error message HybridSynchronizationActiveDirectoryUserPrincipalNameNotUnique"
	infoBubbleText="Workday to AD User Provisioning shows error message HybridSynchronizationActiveDirectoryUserPrincipalNameNotUnique"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629760,32629798"
	productPesIds="16666"
	articleId="8d591007-b474-4b63-9f3e-451f17322ef4"
	CloudEnvironments="Public"
/>

# Workday to AD User Provisioning shows error message HybridSynchronizationActiveDirectoryUserPrincipalNameNotUnique

The Workday to AD User Provisioning Workday to AD User Provisioning shows error message HybridSynchronizationActiveDirectoryUserPrincipalNameNotUnique. *The operation failed because UPN value provided for addition/modification is not unique forest-wide. Error Details: CONSTRAINT_ATT_TYPE - userPrincipalName.*

## Probable Cause

The *userPrincipalName* value that Workday connector is trying to set when creating the AD user account already exists in the target AD domain. This implies that either (1) the user already exists and the matching ID check failed for the user or (2) the UPN generation rule generated a conflicting value.

## Recommended Solution

1. If the user already exists and the matching ID check failed to link the Workday account to Active Directory account, then check if the matching ID attribute (typically: employeeID) in both Workday and AD have an exact match. If they don't have a match, it is a data issue that needs to be fixed. For e.g. if the EmployeeID in Workday is 001052 and in AD it is 1052, then the provisioning engine will fail to link the two accounts and try to create a user that already exists. The solution in this case is to change the EmployeeID value in AD to include the leading zeros to make it 001052.
1. If the UPN generating expression is not generating a unique value, consider using the de-duplication function *[SelectUniqueValue](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/functions-for-customizing-application-data#selectuniquevalue)* to generate a unique value each time.

## Recommended Documents

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
