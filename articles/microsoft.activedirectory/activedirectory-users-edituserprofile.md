<properties 
    pageTitle="I can't edit a user profile in my Azure AD"
    description="I can't edit a user profile in my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    ms.author="Jeffsta-MSFT"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32615378"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="bb6b116b-cebb-45b8-a4c3-001ca7c76cf8"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# I can't edit a user profile in my Azure AD

## **Recommended steps**

1. For a user whose source of authority is Windows Server AD, update [synchronized properties](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-sync-attributes-synchronized) for the user in Windows Server AD, and wait for the next synchronization cycle to complete. Then the updated properties will be visible in Azure AD.<br>
2. Only a Global administrator or User administrator of Azure AD can update most properties of a user in Azure AD. If you are not in one of these roles, you must have an administrator update the properties for you or add you to one of these roles.<br>
3. Only a Global administrator can update authentication contact info for another user. A user can update their own authentication contact info on their [Access Panel Profile](https://account.activedirectory.windowsazure.com/r/#/profile).<br>

## **Recommended documents**

* [Update user profile info in the Azure AD admin portal experience](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)<br>
* [Use Azure AD PowerShell to update profile properties for a user](https://docs.microsoft.com/powershell/module/azuread/Set-AzureADUser?view=azureadps-2.0)<br>
* [Use Azure AD PowerShell to set the manager for a user](https://docs.microsoft.com/powershell/module/azuread/set-azureadusermanager?view=azureadps-2.0)<br>
* [Use Azure AD PowerShell to set the thumbnail photo for a user](https://docs.microsoft.com/powershell/module/azuread/set-azureaduserthumbnailphoto?view=azureadps-2.0)