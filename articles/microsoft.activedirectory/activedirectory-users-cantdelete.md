<properties 
    pageTitle="Problem deleting a user"
    description="Problem deleting a user"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    ms.author="Jeffsta-MSFT"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32586793"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="af9602ba-90c1-4183-9407-922b87ed1326"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>
# I can't delete a user in my directory

## **Recommended steps**

1. Ensure that you are authorized to delete a user. Only the Global Administrator or User Account Administrator role in Azure AD can perform these tasks. If you are not in one of these roles, ask an administrator to delete the user for you or to add you to one of these roles.<br>
2. If the user you need to delete is synchronized from your Windows Server AD using Azure AD Connect, you must first delete the user in Windows Server AD. The user will be deleted in Azure AD after the next synchronization cycle is complete.<br>

### **Recommended tools**

* See the [Azure AD roles and administrators](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RolesAndAdministrators) for your Azure AD.<br>
* See the [deleted users](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UsersManagementMenuBlade/DeletedUsers) in your Azure AD.<br>

## **Recommended documents**

* [Delete a user in the Azure portal](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory#delete-a-user)<br>
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)<br>
* [Use PowerShell to delete a user](https://docs.microsoft.com/powershell/azuread/v2/set-azureaduser)<br>
* [Use PowerShell to permanently delete a user by removing the user from the recycle bin](https://docs.microsoft.com/powershell/module/MSOnline/Remove-MsolUser?view=azureadps-1.0#optional-parameters)
