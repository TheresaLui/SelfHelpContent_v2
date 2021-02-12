<properties 
    pageTitle="Group expiration"
    description="Group expiration"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="yyuank"
    ms.author="yukarppa"
    selfHelpType="generic"
    supportTopicIds="32615385"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="4e01b60c-bf2f-4d15-a8b0-09ac8f5bbf13"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Group expiration

## **Recommended Steps**

### **Expiration policy configuration**<br>
1. This functionality is only supported for Office 365 groups. Security groups and distribution groups are not supported.
2. Configuring and using the expiration policy for Office 365 groups requires an Azure AD Premium license
3. Currently only one expiration policy can be configured for Office 365 groups on a tenant
4. Only Global administrators, Group administrators, User administrators, and the owner of the group are able to renew a group
5. If an Office 365 group is expired, it is deleted and can only be restored up to 30 days before permanent deletion occurs. Once permanently deleted, the group can no longer be restored. Learn more about restoring groups [here](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-restore-deleted).<br>

### **Activity-based automatic renewal**<br>

User activities from SharePoint, Outlook and Teams can trigger group automatic renewal. Activities are checked at 35 days before a group expires. If there is activity during the current group lifecycle, the group will be automatically renewed and email notification won't be sent out to group owners.

### **Notification Timing for Expired groups**<br>

1. Email notifications are sent to the Office 365 group owners 30 days, 15 days, and 1 day prior to expiration of the group
2. When you first set up expiration, any groups that are older than the expiration interval are set to 35 days until expiration
3. Group expiration date is calculated based on the group’s renewal date, not based on the policy updated date. If the expiration policy is updated, the expiration date will not change


## **Recommended Documents**

* [Group Expiration policy and renewal emails](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-lifecycle) 
* [Restore a deleted Office 365 group in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-restore-azure-portal)

### **Recommended Videos**
* [Advanced features of group management: group expiration, dynamic groups, and group naming policy](https://www.youtube.com/watch?v=e9zUqQx5upY)
