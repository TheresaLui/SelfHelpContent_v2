<properties 
    pageTitle="Group expiration"
    description="Group expiration"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="krbain"
    selfHelpType="generic"
    supportTopicIds="32615385"
    productPesIds="16578"
    cloudEnvironments="public"
/>

# Group expiration

## **Recommended steps**

**Expiration policy configuration**<br>
1. This functionality is only supported for Office 365 groups. Security groups and distribution groups are not supported.<br>
2. Configuring and using the expiration policy for Office 365 groups requires an Azure AD Premium license.<br>
3. Currently only one expiration policy can be configured for Office 365 groups on a tenant.<br>
4. Only Global administrators, User account administrators, and the owner of the group are able to renew a group.<br>
5. If an Office 365 group is expired, it is deleted and can only be restored up to 30 days before permanent deletion occurs. Once permanently deleted, the group can no longer be restored. Learn more about restoring groups [here](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-restore-azure-portal).<br>

**Notification Timing for Expired groups**<br>
1. Email notifications are sent to the Office 365 group owners 30 days, 15 days, and 1 day prior to expiration of the group.<br>
2. When you first set up expiration, any groups that are older than the expiration interval are set to 30 days until expiration and the first renewal notification is sent within a day of set up.<br>
3. Group expiration date is calculated based on the group’s renewal date not based on policy updated date, so if the expiration policy is updated, the first notification will be sent 30 days from the newly calculated renewal date. If that date has already passed, the notification will be received 30 days from the current date.<br>
4. Dynamic membership groups are re-populated after they are restored and renewal is re-calculated, so users may receive another renewal notification.<br>


## **Recommended documents**
* [Group Expiration policy and renewal emails](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-lifecycle) 
* [Restore a deleted Office 365 group in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-restore-azure-portal)
