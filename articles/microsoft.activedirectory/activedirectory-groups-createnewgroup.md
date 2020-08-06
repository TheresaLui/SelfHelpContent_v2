<properties 
    pageTitle="Creating a new group"
    description="Creating a new group"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="krbain"
    ms.author="jupetter"
    selfHelpType="generic"
    supportTopicIds="32586792"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="96948e70-b956-4bf2-bf63-6085f73bb4f0"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Creating a new group

## **Recommended Steps**

**Permission to Create a Group**<br>
Ensure you are authorized to create a new group. Global administrators can disable group creation in the Azure portal or Access Panel. You may need an administrator create the new group for you, or give you appropriate permissions.<br>

**Manage Group creation permissions**<br>
1. Global administrators can manage group creation permissions for security or Office 365 groups created in the Azure portal or Access Panel, by setting "Users can create security groups in Azure portals" or "Users can create Office 365 groups in Azure portals" settings in **All groups > General (Settings)**.<br>
2. You can also restrict group creation to select a group of users if you have an Azure Active Directory P1 Premium license.<br>

**Disabling welcome notification for new Office 365 group members**<br>
The welcome notification sent to users who are added to Office 365 groups can be disabled by setting the UnifiedGroupWelcomeMessageEnabled to False in Powershell. Learn about this setting [here](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Set-UnifiedGroup?view=exchange-ps).<br>

## **Recommended Documents**

* [Create a new group and add members in Azure portal](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
* [Create groups in Powershell MSOnline](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-v2-cmdlets#create-groups)
* [Disable groups creation in Powershell](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-v2-cmdlets#disable-group-creation-by-your-users)
* [Manage who can create groups in Office 365](https://support.office.com/article/Manage-who-can-create-Office-365-Groups-4c46c8cb-17d0-44b5-9776-005fced8e618)
* [Disable Office 365 welcome notification via Powershell](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Set-UnifiedGroup?view=exchange-ps)
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)

### **Recommended Videos**

* [Group management: learn about group functionalities and the latest features for AAD groups](https://www.youtube.com/watch?v=H6aZs0Q-kOA)
* [Advanced features of group management: group expiration, dynamic groups, and group naming policy](https://www.youtube.com/watch?v=e9zUqQx5upY)
