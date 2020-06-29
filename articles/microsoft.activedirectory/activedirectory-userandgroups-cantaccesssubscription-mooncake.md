<properties
    pageTitle="I can’t access an Azure subscription"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
	ms.author="curtand"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview,userandgroups_user"
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="activedirectory-userandgroups-cantaccesssubscription-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I can’t access an Azure subscription

## **Recommended Steps**

1. If you are unable to access an Azure subscription, ensure that your role in the Azure AD is authorized to manage the tenant and is given permissions on that specific subscription. If you need to assign access to an Azure subscription, such as a virtual machine, navigate to the Azure resource and assign access there. Learn more about [Azure AD permissions and roles](https://docs.azure.cn/active-directory/users-groups-roles/directory-assign-admin-roles#administrator-permissions).

2. Ensure that you are given permissions on the Azure subscription you are trying to access, if you have an Azure AD role assignment that does not convey that you have automatic permission on the subscriptions in that Azure AD.  Learn more about [Assigning access to Azure resources](https://docs.azure.cn/role-based-access-control/role-assignments-portal#add-access).

## **Recommended Documents**

* [Use PowerShell to add a user to an Azure AD role](https://docs.microsoft.com/powershell/azuread/v2/add-azureaddirectoryrolemember)
* [Use PowerShell to manage access to Azure subscription resources](https://docs.azure.cn/role-based-access-control/role-assignments-powershell)

