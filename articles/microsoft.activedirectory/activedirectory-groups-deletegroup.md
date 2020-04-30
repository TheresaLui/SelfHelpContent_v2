<properties 
    pageTitle="Deleting a group"
    description="Deleting a group"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="yyuank"
    ms.author="yukarppa"
    selfHelpType="generic"
    supportTopicIds="32615372"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="d326a858-7a12-4e34-bc6c-3277b2fe5866"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Deleting a group

## **Recommended Steps**

### **Delete a group**

1. Groups can be deleted from the directory using the [Remove-AzureADGroup cmdlet in the Azure AD Powershell module](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-v2-cmdlets#delete-groups)
2. Before attempting to delete a synced group in Azure Active Directory, ensure you have [deleted all assigned licenses](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-group-advanced#deleting-a-group-with-an-assigned-license) to avoid errors

### **Restore a deleted group**

1. If an Office 365 group is deleted, it can only be restored up to 30 days before permanent deletion occurs. Once permanently deleted, the group can no longer be restored. Learn more about restoring groups [here](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-restore-azure-portal).<br>
2. This functionality is not supported for security groups and distribution groups
3. Ensure you are authorized to restore an Office 365 group. Global administrators, Group administrators, User account administrators, Intune service administrators, Partner Tier1 or Tier2 support, and the owner of the group are able to restore a group.<br>
4. When a dynamic group is deleted and restored, it is seen as a new group and re-populated according to the rule. This process might take up to 24 hours.<br>

## **Recommended Documents**

* [Deleting a group with an assigned license](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-group-advanced#deleting-a-group-with-an-assigned-license)
* [Restore a deleted Office 365 group in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-restore-azure-portal) 
