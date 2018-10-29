<properties 
    pageTitle="Other problems managing a user"
    description="Other problems managing a user"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32565604"
    productPesIds="14785"
    cloudEnvironments="public"
    />


# I can't update the properties of a user in my Azure AD tenant

## **Recommended steps**

1. If you need to leave a directory to which you have been invited as a guest, you can do you on your [profile page](https://account.activedirectory.windowsazure.com/r#/profile). In the **Organizations** section on that page, find the directory you want to leave, and select **Sign in to leave organization**.
2. Ensure that you are authorized to perform the task. Only the Global Administrator or User Account Administrator roles can update user properties. If you are not in one of these roles, you must ask an administrator to update the user properties for you, or add you to one of these roles. You can see the administrators of your Azure AD directory on the [Roles and administrators](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RolesAndAdministrators) page of your directory.
3. If you need to update a synchronized user, update the properties in Windows Server AD. The changes are automatically synchronized every 15 minutes. Attributes synchronized by [Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-attributes-synchronized) can be changed only in Windows Server Active Directory.
4. Many user management tasks can be completed using Azure AD PowerShell cmdlets. To see all the capabilities of these cmdlets, read our [PowerShell reference for user management](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0#users).

## **Recommended documents**

* [Use the Azure portal to change profile information for a user](https://docs.microsoft.com/azure/active-directory/active-directory-users-profile-azure-portal)<br>
* [Use PowerShell to update profile properties for a user](https://docs.microsoft.com/powershell/azuread/v2/set-azureaduser)<br>
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)