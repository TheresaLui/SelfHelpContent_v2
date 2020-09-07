<properties
    pageTitle="Problems with RBAC role assignments"
    description="Azure Active Directory troubleshooting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    ms.author="rolyon"
    displayOrder=""
    articleId="694d1932-31de-4b5b-b393-22a52c75d533"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32690724"
    resourceTags=""
    productPesIds="16986"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="AzureIdentity_RBAC"
/>

# Azure Active Directory: Problems with RBAC role assignments

## **Recommended Steps**

* If you are unable to add a role assignment in the Azure portal on **Access control (IAM)** because the **Add** > **Add role assignment** option is disabled or because you get the permissions error "The client with object id does not have authorization to perform action", check that you are currently signed in with a user that is assigned a role that has the *Microsoft.Authorization/roleAssignments/write* permission such as [Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner) or [User Access Administrator](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#user-access-administrator) at the scope you are trying to assign the role
* If you get the permissions error "The client with object id does not have authorization to perform action over scope (code: AuthorizationFailed)" when you try to create a resource, check that you are currently signed in with a user that is assigned a role that has write permission to the resource at the selected scope. For example, to manage virtual machines in a resource group, you should have the [Virtual Machine Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#virtual-machine-contributor) role on the resource group (or parent scope). For a list of the permissions for each built-in role, see [Built-in roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles).
* If you get the permissions error "You don't have permission to create a support request" when you try to create or update a support ticket, check that you are currently signed in with a user that is assigned a role that has the *Microsoft.Support/supportTickets/write* permission, such as [Support Request Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#support-request-contributor)
* If you get the error message  "No more role assignments can be created (code: RoleAssignmentLimitExceeded)" when you try to assign a role, try to reduce the number of role assignments by assigning roles to groups instead. Azure supports up to **2000** role assignments per subscription.

## **Recommended Documents**

- [Manage access to Azure resources using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)
- [Built-in roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
