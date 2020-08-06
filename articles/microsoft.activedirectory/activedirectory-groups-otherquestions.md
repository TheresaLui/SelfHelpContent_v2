<properties 
    pageTitle="Other questions about managing groups"
    description="Other questions about managing groups"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="krbain"
    selfHelpType="generic"
    supportTopicIds="32586794"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="a864c970-4787-4cc0-ad47-ef2c5ac18f7b"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Other questions about managing groups

## **Recommended steps**

**Disabling welcome notification for new Office 365 group members**<br>
The welcome notification sent to users who are added to Office 365 groups can be disabled by setting the **UnifiedGroupWelcomeMessageEnabled** to False in Powershell. Learn about this setting [here](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Set-UnifiedGroup?view=exchange-ps).

**Manage Group creation permissions**<br>
1. Global administrators can manage group creation permissions for security or Office 365 groups in the Azure portal or Access Panel, by setting "Users can create security groups in Azure portals" or "Users can create Office 365 groups in Azure portals" settings in **All groups > General (Settings)**.<br>
2. You can also restrict group creation to select a group of users if you have an Azure Active Directory P1 Premium license.<br>

**Troubleshooting Nested groups**<br>
1. Currently, nesting a group as member of another group is only supported for security groups, it is not supported for Office 365 groups at this time.<br>
2. Nested group memberships are not supported for group-based assignment to applications at this time. Learn more about SaaS application support [here](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-saasapps).<br>
3. [Group-based licensing](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-group-advanced#limitations-and-known-issues) currently does not support groups that contain other groups (nested groups). If you apply a license to a nested group, only the immediate first-level user members of the group have the licenses applied.<br>

## **Recommended documents**

* [Disable groups creation in Powershell](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-v2-cmdlets#disable-group-creation-by-your-users)
* [Manage who can create groups in Office 365](https://support.office.com/article/Manage-who-can-create-Office-365-Groups-4c46c8cb-17d0-44b5-9776-005fced8e618)
* [Disable Office 365 welcome notification via Powershell](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Set-UnifiedGroup?view=exchange-ps)
