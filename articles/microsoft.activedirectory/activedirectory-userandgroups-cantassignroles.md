<properties
    pageTitle="I can’t assign roles to other users in the Azure AD tenant"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
	ms.author="curtand"
    displayOrder="4294"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview,userandgroups_user"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="2eec419f-9c11-4a06-90cf-63ff4aa23a6d"
	ownershipId="AzureIdentity_User"
/>

# I can’t assign roles to other users in the Azure AD tenant

## **Recommended steps**
1. Ensure that you are assigned to a directory role that is authorized to manage roles in your current Azure AD. If you are managing multiple directories, verify the tenant you are accessing has given permissions to the Global Administrator or Privileged Identity Manager. In the case, you are given permissions to an Azure subscription that does not convey that you have permissions to manage the Azure AD that is associated with that subscription. Learn more on [Assigning Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles-azure-portal).
2. Assign the role that corresponds to the permissions that the user needs in your Azure AD. To assign the role, navigate to the ‘directory role’ tab for the user. Learn about the [Azure AD permissions and roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles-azure-portal#administrator-permissions).

## **Recommended documents**

* [Use PowerShell to add a user to an Azure AD role](https://docs.microsoft.com/powershell/azuread/v2/add-azureaddirectoryrolemember)
* [Use PowerShell to manage access to Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-access-powershell)

