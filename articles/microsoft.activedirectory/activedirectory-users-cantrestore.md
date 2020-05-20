<properties 
    pageTitle="I can't restore a deleted user in my Azure AD"
    description="I can't restore a deleted user in my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    ms.author="Jeffsta-MSFT"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32615430"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="aa375ab2-1977-40e8-b772-097008394a91"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# I can't restore a deleted user in my Azure AD

## **Recommended steps**

1. For a user whose source of authority is Windows Server AD, restore the deleted user from the recycle bin in Windows Server AD, and wait for the next synchronization cycle to complete. If Recycle Bin is not enabled for your Windows Server AD, restore the user from backup and perform an authoritative restore on the object (if all attribute values are needed) or restore using the Windows Sysinternals tool AdRestore.exe [according to the  documentation](https://support.microsoft.com/help/840001/how-to-restore-deleted-user-accounts-and-their-group-memberships-in-ac).
2. For a user whose source of authority is Azure AD, you can restore a deleted user on the [deleted users](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UsersManagementMenuBlade/DeletedUsers) page of the Azure portal for up to 30 days after the user was deleted. After 30 days, or after the user is permanently deleted by an administrator, neither an administrator nor Microsoft Customer Support can restore the user. Only a Global administrator or User administrator of Azure AD can restore a deleted user. If you are not in one of these roles, you must have an administrator restore the user for you or add you to one of the required roles.<br>

  AdRestore is a Sysinternals tool to simply delete the isDeleted attribute and make it visible in AD. However, most important attributes like group membership are not recovered using this method. If AD Recycle Bin is enabled, you can simply restore from the deleted objects container with all attributes. If they don't have it enabled and need all attributes, they would either need to find a DC that hasn't replicated in the deletion yet and perform an authoritative restore or restore the system state backup from a DC prior to the deletion and then perform an authoritative restore.

### **Recommended tools**

* See the [deleted users](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UsersManagementMenuBlade/DeletedUsers) in your Azure AD. <br>
* See the [Azure AD roles and administrators](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RolesAndAdministrators) for your Azure AD.

## **Recommended documents**

* [Restore a deleted Azure AD user in the Azure AD admin portal experience](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-restore)<br>
* [Use PowerShell to restore a deleted user](https://docs.microsoft.com/powershell/module/msonline/restore-msoluser?view=azureadps-1.0)