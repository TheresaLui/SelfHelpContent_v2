<properties
    pageTitle="Troubleshooting Management groups and subscriptions RBAC permissions"
    description="Common issues with using management groups and subscriptions RBAC Permissions"
    service="Microsoft.Management"
    resource="managementgroups"
    authors="rthorn17"
    ms.author="rithorn"
    articleId="managementgroups-rbac"
    selfHelpType="generic"
    supportTopicIds="32743304"
    productPesIds="16530"
    cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
    ownershipId="ARM_ManagementGroups"
/>

# Management group troubleshooting Role Based Access Control (RBAC) Permissions

## Management groups Role Based Access Control (RBAC) troubleshooting

Management groups are a hierarchical structure of groups that allow you to build a tree of inherited RBAC permissions. Having multiple tiers of inheritance can cause confusion and sometimes issues.  To help troubleshoot these items, we have listed some of the common issues reported with management group and RBAC Accesses.  

## **Recommended Steps**

A majority of issues when moving a subscription/ management group have to do with the permissions you have on the subscription or management group.  Use these recommend steps to make sure you have the correct permissions.

1. Go to the subscription, or child management group, you are trying to move and see what permissions you have. To move a child subscription or management group, **you are required to have general write permissions and role assignment write permissions.** An example built in role and most commonly assigned role, is "Owner" as this role has the ability to create/update/delete management groups along with the ability to create and delete User Role Assignments.

1. Check the current parent management group of the subscription or management group you are trying to move for your permissions. To move a subscription or management group, **you need to have write access on the current parent management group.**  You should have "Owner", "Contributor", "Management Group Contributor" roles or equivalent custom role on the group.  

    * **Exception**: If the current parent management group is the root management group of the hierarchy, the service will not check this permission as this is the default location  

1. Check the target parent management group you are trying to move the subscription or management group to for your permissions. To move a subscription or management group, **you need to have write access on the target parent management group.**  You should have "Owner", "Contributor", "Management Group Contributor" roles or equivalent custom role on the group.

    * **Exception**: If the target parent management group is the root management group of the hierarchy, the service will not check this permission as this is the default location

With these three permissions being true, you will be able to move the subscription or management group between different management groups. For more information, see [How to change, delete, or manage your management groups](https://docs.microsoft.com/azure/governance/management-groups/manage#moving-management-groups-and-subscriptions).

## Inherited Access

A feature of using management group is the ability for Role Based Access controls (RBAC) roles to be inherited down the hierarchy tree.  A Role Assignment that is done on a management group will automatically be applied to all management groups, subscriptions, resource groups, and resources that are descendant of that management group.  This provides ease of use and security as there is only one role assignment that is needed instead of multiple assignments at each resource or scope. Since there is only one assignment, it becomes easier to maintain the assignment if it becomes outdated.  

With this inheritance also comes the risk that heightened privileges can be assigned to a top level management group and it will be applied to unexpected resources. For example, assigning a user an "Owner" role on the Root Management Group will give that user "Owner" permissions to all children of that Root.  

To check who has inherited access to your resource and where it is assigned:

- Login to the Azure portal
- Navigate to the management group, subscription, resource group, or resource detail page
- Select the **Access control (IAM)** on the left navigation menu
- Select the **Role Assignment** tab
- Under the **Scope** column, any role assignment listed **Management group (Inherited)** is an inherited role assignment
- Hovering your mouse over the link **Management group (Inherited)** lets you see the hierarchy path where the assignment has been inherited from

## The subscription or management group is not listed

When working within the Azure portal, the dropdowns will only show you the items you are able to move.  This is to help avoid any errors as the service only will present the items with the proper permissions.  If you are not seeing the proper items in the dropdowns, check your permissions on the subscriptions or management groups. For help see the recommended steps above on how to check your permissions.  

## I can't see the subscription that I just moved

If you are having trouble finding the subscription you just moved under a management group, there are a couple steps you can do to find out what happened.  

- Check the notifications section in the portal to see if there was a failure. If the process of moving the subscription failed, you will see an error in the notifications. You can find the notifications window in the upper right hand corner of the Azure portal with the icon of a bell.
- Check the default subscription filter to make sure the subscription you are looking for is enabled in the views. You can find the Directory + subscription filter window in the upper right hand corner of the Azure portal with the icon of a notebook with the filter icon on top of it.
- Check your permission on the new management group and the subscription itself. While you needed the proper permissions to move the subscription there could have been changes to the role assignments since then. See the recommended steps above on how to check your permissions.
- Was the move done within the last 30 minutes?
  - If so, there could be a user token issue that is preventing the subscription from showing within the Azure portal. Try refreshing the browser and/or logging in and out of the Azure portal. This will renew the user token.
  - If you are on the management group pages within the Azure portal, select the refresh button on the table to refresh the table
  - It could be possible there is a data latency issue with the replications. If you don't see the subscription after 30 minutes then proceed submitting a support request for help.

## How to regain access to a management group

If you remove your own access from the management group and there are no other users with **Role Assignment/ Write** access, you will need to look at the management group's parent within the hierarchy for the next user with the correct permissions. If you follow the parent chain up to the Root Management Group and there are no other assigned users with **Role Assignment/ Write** permissions, you will need to contact your Azure Active Directly (AAD) Global Admins for support. The [AAD Global Admins can elevate their access](https://docs.microsoft.com/azure/role-based-access-control/elevate-access-global-admin) to have **Role Assignment/Write** access over the tenant and give you back your access.  

It is suggested that you consider this scenario and implement a "Break Glass" action where a user at a high level management group can gain access to the group and assign users roles if needed. Having this process typically includes a Just In Time (JIT) practice, multi- turn key authorization, or overall segregation of duties authorization to minimize risk.

## Custom RBAC roles and management groups

Custom RBAC role support for management groups is currently supported with some [limitations](https://docs.microsoft.com/azure/governance/management-groups/overview#limitations). You can define the management group scope in the Role Definition's assignable scope. That custom RBAC Role will then be available for assignment on that management group and any management group, subscription, resource group, or resource under it. This custom role will inherit down the hierarchy like any built-in role.

[Learn more](https://docs.microsoft.com/azure/governance/management-groups/overview#custom-rbac-role-definition-and-assignment) 

## Issues with Resource Groups

Management groups are different objects in Azure than resource groups.  Resource groups are groupings under the subscription that hold resources directly. Management groups are a grouping construct that are above the subscription level and can only have subscriptions or other management groups as children. For more information on Resource Groups, see [Manage Azure Resource Manager resource groups](https://docs.microsoft.com/azure/azure-resource-manager/manage-resource-groups-portal).

## **Recommended Documents**

- [Management groups move operation permissions](https://docs.microsoft.com/azure/governance/management-groups/overview#moving-management-groups-and-subscriptions)
- [Organize your resources with Azure management groups](https://docs.microsoft.com/azure/governance/management-groups/overview)
- [How to change, delete, or manage your management groups](https://docs.microsoft.com/azure/governance/management-groups/manage)
- [Create management groups to organize Azure resources](https://docs.microsoft.com/azure/governance/management-groups/create)
