<properties 
    pageTitle="I can't restore a deleted user in my Azure AD"
    description="I can't resotre a deleted user in my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authorAlias="Jeffsta-MSFT"
    authors="Jeffsta-MSFT"
    selfHelpType="generic" 
    supportTopicIds="32615430"
    productPesIds="16578"
    cloudEnvironments="public"
 />

# I can't restore a deleted user in my Azure AD

## **Recommended steps**

1. For a user whose source of authority is Windows Server AD, restore the deleted user from the recycle bin in Windows Server AD, and wait for the next synchronization cycle to complete.If recycle bin is not enabled for your Windows Server AD, restore the user from backup or using adrestore.<br>
2. For a user whose source of authority is Azure AD, you can restore a deleted user on the [deleted users](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UsersManagementMenuBlade/DeletedUsers) page of the Azure portal for up to 30 days after the user was deleted. After 30 days, or after the user is permanently deleted by an administrator, neither an administrator nor Microsoft Customer Support can restore the user. Only a global administrator or user administrator of Azure AD can restore a deleted user. If you are not in one of these roles, you must have an administrator restore the user for you, or add you to one of these roles.<br>

### **Recommended tools**

* See the [deleted users](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UsersManagementMenuBlade/DeletedUsers) in your Azure AD. <br>
* See the [Azure AD roles and administrators](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RolesAndAdministrators) for your Azure AD.<br>

## **Recommended documents**

* [Restore a deleted Azure AD user in the Azure AD admin portal experience](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-restore)<br>
* [Use PowerShell to restore a deleted user](https://docs.microsoft.com/powershell/module/msonline/restore-msoluser?view=azureadps-1.0)