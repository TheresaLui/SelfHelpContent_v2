<properties
    pageTitle="I can’t delete a user from my directory"
    description=" I can’t delete a user from my directory"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    ms.author="jeffsta"
    displayOrder="3"
    selfHelpType="resource"
    resourceTags="userandgroups_overview,userandgroups_user"
    cloudEnvironments="MoonCake"
 	articleId="activedirectory-userandgroups-delete-users-troubleshooter-mooncake"
	ownershipId="AzureIdentity_User"
/>
# I can’t delete a user from my directory

## **Recommended Steps**

1. Ensure that you are authorized to delete a user. Only a global administrator or user administrator of Azure AD can delete a user. If you are not in one of these roles, you need to ask an administrator add you to one of these roles, or to delete the user for you.  [Azure AD administrative roles](https://docs.azure.cn/active-directory/users-groups-roles/directory-assign-admin-roles)
2. Ensure that the user is not synced from your on-premises AD. If the user is synced (that is, if Source = ‘Windows Server AD’), then delete the user in your on-premises directory. Then after sync runs, you can see that the user has been deleted from Azure AD.

## **Recommended Documents**

* [Delete a user in the Azure portal](https://docs.azure.cn/active-directory/fundamentals/add-users-azure-active-directory)
* [Azure AD administrative roles](https://docs.azure.cn/active-directory/users-groups-roles/directory-assign-admin-roles)
* [Use Azure AD PowerShell to delete a user](https://docs.microsoft.com/powershell/azuread/v2/remove-azureaduser)
