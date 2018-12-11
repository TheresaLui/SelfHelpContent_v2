<properties
    pageTitle="Problems with custom roles"
    description="Azure Active Directory troubleshooting"
    infoBubbleText=""
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    displayOrder=""
    articleId=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32615422"
    resourceTags=""
    productPesIds="16578"​
    cloudEnvironments="public"
/>

# Problems with custom roles

## Recommended steps

1. If need steps for how to create a custom role, see the custom role tutorials using [PowerShell](https://docs.microsoft.com/azure/role-based-access-control/tutorial-custom-role-powershell) or [CLI](https://docs.microsoft.com/azure/role-based-access-control/tutorial-custom-role-cli).
1. If you are unable to update an existing custom role, check whether you have the Microsoft.Authorization/roleDefinition/write permission.
1. If you are unable to delete a custom role, check whether there are any role assignments still using the custom role. If so, remove those role assignments and try to delete again.
1. If you get an error that the role definition limit exceeded when you try to create a new role, delete any custom roles that aren’t be used. Azure supports up to 2000 custom roles in a tenant.
1. If you get an error that the scope (such as subscription or resource group) was not found when you try to update a custom role, check whether one or more assignable scopes have been deleted in the tenant. If the scope is deleted, then create a support ticket as there is no self-service solution available at this time.

## Recommended documentation

- [Create custom roles using Azure PowerShell](https://docs.microsoft.com/azure/role-based-access-control/custom-roles-powershell)
- [Create custom roles using Azure CLI](https://docs.microsoft.com/azure/role-based-access-control/custom-roles-cli)
- [Custom roles in Azure](https://docs.microsoft.com/azure/role-based-access-control/custom-roles)
