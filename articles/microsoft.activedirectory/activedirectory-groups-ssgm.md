<properties 
    pageTitle="Self-service group management"
    description="Self-service group management"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="krbain"
    selfHelpType="generic"
    supportTopicIds="32615431"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="e273e5a1-8e0f-419d-823e-8cfb4d004764"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Self-service group management

## **Recommended steps**

**Manage access to Access Panel portal**<br>
1. Global administrators can manage access to groups features in the Access Panel, by setting "Restrict access to Groups in the Access Panel" in **All groups > General (Settings)**.<br>
2. Global administrators can also manage the "Owners can manage group membership requests in the Access Panel" setting, if you have an Azure Active Directory P1 Premium license.<br>

**Manage Group creation permissions**<br>
1. Global administrators can manage group creation permissions for security or Office 365 groups in the Azure portal or Access Panel, by setting "Users can create security groups in Azure portals" or "Users can create Office 365 groups in Azure portals" settings in **All groups > General (Settings)**.<br>
2. You can also restrict group creation to select a group of users if you have an Azure Active Directory P1 Premium license.<br>

**Manage ownership assignment privileges**<br>
Global administrators can restrict group ownership assignment privileges to a select a group of users using the "Owners who assign members as groups owners in Azure portals" settings for security or Office 365 groups.

## **Recommended documents**

* [Disable groups creation in Powershell](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-v2-cmdlets#disable-group-creation-by-your-users)
* [Manage who can create groups in Office 365](https://support.office.com/article/Manage-who-can-create-Office-365-Groups-4c46c8cb-17d0-44b5-9776-005fced8e618)
