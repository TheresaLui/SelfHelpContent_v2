<properties
    pageTitle="Problem deciding which Azure AD role to assign"
    description="Azure AD Roles and administration"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615408"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="cad8aaca-5511-4d85-bfbe-ce5aaa78ebaf"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem deciding which Azure AD role to assign

## **Recommended steps**

* Review the [list of roles](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) that are available for assignment in Azure AD.<br>
* Determine which Azure AD resources the user needs to manage, and identify the Azure AD role that has the minimum permissions that enable a user to manage those resources. You need to choose from the list of available roles. It is not possible for an administrator to create new roles in Azure AD, or to modify the permissions of the built-in roles.<br>
* Assign the Azure AD role to the user. You can do this on the 'Members' page for the Azure AD role, or on the 'Directory role' page for the user. 

## **Recommended documents**

* [Azure AD role permissions reference](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)<br>
* [Understand the difference between Azure AD roles and Azure RBAC roles](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles)<br>
* [Assign an Azure AD role to a user](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)
