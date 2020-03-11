<properties 
    pageTitle="I can't create a new user in my Azure AD"
    description="I can't create a new user in my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    ms.author="jeffsta"
    displayOrder="4"
    selfHelpType="resource"
    resourceTags="userandgroups_overview,userandgroups_user"
    cloudEnvironments="MoonCake"
 	articleId="activedirectory-userandgroups-create-users-troubleshooter-mooncake"
	ownershipId="AzureIdentity_User"
/>
# I can’t create a new user in my Azure AD

## **Recommended Steps**
1. Ensure that you are authorized to create a new standard user. Only a global administrator or user administrator of Azure AD can create a new standard user. If you are not in one of these roles, you must have an administrator create the new user for you, or add you to one of these roles.  [Azure AD administrative roles](https://docs.azure.cn/active-directory/users-groups-roles/directory-assign-admin-roles)
2. Ensure that the user name is in a domain that is not federated to Azure AD from your on-premises AD. Users cannot be added in the cloud with domain names that are federated with your Azure AD.
3. Ensure that no other user or contact already has the user name that you want to assign to the new user. User names must be unique across Azure AD.

## **Recommended Documents**

* [Use the Azure portal to create a new user in your Azure AD](https://docs.azure.cn/active-directory/fundamentals/add-users-azure-active-directory) 
* [Azure AD administrative roles](https://docs.azure.cn/active-directory/users-groups-roles/directory-assign-admin-roles) 
* [Use Azure AD PowerShell to create a new user](https://docs.microsoft.com/powershell/azuread/v2/new-azureaduser)

