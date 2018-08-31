<properties 
    pageTitle="Other questions about managing groups"
    description="Other questions about managing groups"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="krbain"
    selfHelpType="generic"
    supportTopicIds="32586794"
    productPesIds="14785"
    cloudEnvironments="public"
/>
  
# Other questions about managing groups

## **Recommended steps**

**Disabling welcome notification for new Office 365 group members**<br>
The welcome notification sent to users who are added to Office 365 groups can be disabled by setting the UnifiedGroupWelcomeMessageEnabled to False in Powershell. Learn about this setting [here](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Set-UnifiedGroup?view=exchange-ps).

**Manage Group creation permissions**<br>
* Global administrators can manage group creation permissions for security or Office 365 groups in the Azure portal or Access Panel, by setting "Users can create security groups in Azure portals" or "Users can create Office 365 groups in Azure portals" settings in **All groups > General (Settings)**. 
* You can also restrict group creation to select a group of users if you have an Azure Active Directory P1 Premium license.

**Troubleshooting Nested groups**<br>
1. Currently, nesting a group as member of another group is only supported for security groups, it is not supported for Office 365 groups at this time.<br>
2. Nested group memberships are not supported for group-based assignment to applications at this time. Learn more about SaaS application support [here](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-saasapps).<br>
3. [Group-based licensing](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-group-advanced#limitations-and-known-issues) currently does not support groups that contain other groups (nested groups). If you apply a license to a nested group, only the immediate first-level user members of the group have the licenses applied.<br>

**Unable to restore a deleted group**<br>
* If an Office 365 group is deleted, admins it can only be restored up to 30 days before permanent deletion occurs. Once permanently deleted, the group can no longer be restored. Learn more about restoring groups [here](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-restore-azure-portal).<br>
* This functionality is not supported for security groups and distribution groups.<br>
* Ensure you are authorized to restore an Office 365 group, only Global administrators, User account administrators, Intune service administrators, Partner Tier1 or Tier2 support and the owner of the group are able to restore a group.<br>

**Notification Timing for Expired groups**<br>
1. Email notifications are sent to the Office 365 group owners 30 days, 15 days, and 1 day prior to expiration of the group.<br>
2. When you first set up expiration, any groups that are older than the expiration interval are set to 30 days until expiration and the first renewal notification is sent within a day of set up.<br>
3. Group expiration date is calculated based on the group’s renewal date not based on policy updated date, so if the expiration policy is updated, the first notification will be sent 30 days from the newly calculated renewal date. If that date has already passed, the notification will be received 30 days from the current date.<br>
 4. Dynamic membership groups are re-populated after they are restored and renewal is re-calculated, so users may receive another renewal notification.<br><br>


## **Recommended documents**

* [Disable groups creation in Powershell](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-v2-cmdlets#disable-group-creation-by-your-users)
* [Manage who can create groups in Office 365](https://support.office.com/article/Manage-who-can-create-Office-365-Groups-4c46c8cb-17d0-44b5-9776-005fced8e618)
* [Restore a deleted Office 365 group in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-restore-azure-portal)
* [Group Expiration policy and renewal emails](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-lifecycle) 
* [Disable Office 365 welcome notification via Powershell](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Set-UnifiedGroup?view=exchange-ps) 
