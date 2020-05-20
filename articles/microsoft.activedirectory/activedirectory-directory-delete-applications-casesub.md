<properties
    pageTitle="Problems removing applications"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615412"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="760ef8f7-8b2e-417c-b563-0214d24cbd6f"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Directory eletion problem with removing applications

## **Recommended steps**

1. Ensure you do not have any multi-tenanted applications configured in your Azure AD. If you have enterprise apps or other app registrations in your tenant that are provisioned in another tenant ensure that they are not linked to the tenant you are trying to delete. Learn more about [Deleting an enterprise application](https://docs.microsoft.com/azure/active-directory/manage-apps/remove-user-or-group-access-portal#how-do-i-remove-a-user-or-group-assignment-to-an-enterprise-app-in-the-azure-portal).
2. To change the configuration of any application, ensure that you have the correct access in the tenant and it corresponds to the permissions required to make the changes in your Azure AD. To assign the role, navigate to the ‘directory role’ tab for the user. [Ensure you are assigned the proper role to make changes on applications](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal).
3. If you are failing to see the application that is blocking the tenant deletion in the Azure portal, navigate to PowerShell to retrieve the list of apps configured in your Azure AD. [List all applications in Azure AD if not showing up in the Azure portal](https://docs.microsoft.com/azure/active-directory/manage-apps/remove-user-or-group-access-portal#how-do-i-remove-a-user-or-group-assignment-to-an-enterprise-app-using-powershell).

## **Recommended documents**
* [How to manage apps in Azure AD](https://docs.microsoft.com/azure/active-directory/manage-apps/remove-user-or-group-access-portal#next-steps)
* [Using PowerShell to delete apps](https://docs.microsoft.com/powershell/module/azuread/remove-azureadapplication?view=azureadps-2.0)
