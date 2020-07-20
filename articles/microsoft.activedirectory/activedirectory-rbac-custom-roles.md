<properties
    pageTitle="Problems with custom roles"
    description="Azure Active Directory troubleshooting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    ms.author="rolyon"
    displayOrder=""
    articleId="b8319a48-eb00-4df4-b621-f01f1d2c9117"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32690723"
    resourceTags=""
    productPesIds="16986"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="AzureIdentity_RBAC"
/>

# Azure Active Directory: Problems with custom roles

## **Recommended Steps**

* If you need steps for how to create a custom role, see the custom role tutorials using [Azure PowerShell](https://docs.microsoft.com/azure/role-based-access-control/tutorial-custom-role-powershell) or [Azure CLI](https://docs.microsoft.com/azure/role-based-access-control/tutorial-custom-role-cli)
* If you are unable to update an existing custom role, check that you are currently signed in with a user that is assigned a role that has the *Microsoft.Authorization/roleDefinition/write* permission such as [Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner) or [User Access Administrator](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#user-access-administrator)
* If you are unable to delete a custom role and get the error message "There are existing role assignments referencing role (code: RoleDefinitionHasAssignments)", then there are role assignments still using the custom role. Remove those role assignments and try to delete the custom role again.
* If you get the error message "Role definition limit exceeded. No more role definitions can be created (RoleDefinitionLimitExceeded)" when you try to create a new custom role, delete any custom roles that aren't being used. Azure supports up to **5000** custom roles in an Azure AD tenant. (For specialized clouds, such as Azure Government, Azure Germany, and Azure China 21Vianet, the limit is 2000 custom roles.)
* If you get an error similar to "The client has permission to perform action 'Microsoft.Authorization/roleDefinitions/write' on scope '/subscriptions/{subscriptionid}', however the linked subscription was not found" when you try to update a custom role, check whether one or more assignable scopes have been deleted in the tenant. If the scope was deleted, then create a support ticket as there is no self-service solution available at this time. 

## **Recommended Documents**

- [Create custom roles for Azure resources using Azure PowerShell](https://docs.microsoft.com/azure/role-based-access-control/custom-roles-powershell)
- [Create custom roles for Azure resources using Azure CLI](https://docs.microsoft.com/azure/role-based-access-control/custom-roles-cli)
- [Custom roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/custom-roles)
