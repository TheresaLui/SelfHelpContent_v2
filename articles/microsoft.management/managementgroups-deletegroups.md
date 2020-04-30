<properties
    pageTitle="Troubleshooting management group deletion"
    description="Common issues with deleting management groups"
    service="Microsoft.Management"
    resource="managementgroups"
    authors="rthorn17"
    ms.author="rithorn"
    articleId="managementgroups-deletegroups"
    selfHelpType="generic"
    supportTopicIds="32609538"
    productPesIds="16530"
    cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
    ownershipId="ARM_ManagementGroups"
/>

# Management group delete troubleshooting

When deleting a management group from the hierarchy you need to make sure there are no children management groups or subscriptions under that group. This is to prevent any accidental deletion that would delete a whole branch of your hierarchy. You need to have delete permissions on the management group and the role assignment to perform the action.  

A management group is permanently delete when the action is performed. This means it cannot be restored if it is done accidentally. You are able to create a new management group with the same ID after it is deleted if needed.

## **Recommended Steps**

### Check if there are any children of the management group  

Go to the subscription or child management group you are trying to delete and see what children it has.

**Portal**

1. Navigate to the management group service page (Main Menu -> All Services -> Management groups)
1. Search for the management group you are trying to delete
1. Select the group name
1. Select details
1. The list shown should be empty. If not, you will need to move those items to another location prior to deleting.

**PowerShell**

1. In the PowerShell command window, enter the command `Get-AzManagementGroup -GroupName [MG ID] -expand`
1. The **Children** parameter should have an empty array. If not, you will need to move those items to another location prior to deletion. 

### Check user access on the management group

Go to the subscription, or child management group, you are trying to delete and see what permissions you have.

**Portal**

1. Navigate to the management group service page (Main Menu -> All Services -> Management groups)
1. Search for the management group you are trying to delete
1. Select the group name
1. Select details
1. Select **Access Control (IAM)**
1. Select **Role Assignments** tab
1. Check your logged in user's permissions for management group delete permissions

**PowerShell**

1. In the PowerShell command window, enter the command `Get-AzRoleAssignment -scope "/providers/microsoft.management/managementgroups/[mgid]"`
1. Check your logged in user's permissions for management group delete permissions  

For more information see, [How to change, delete, or manage your management groups](https://docs.microsoft.com/azure/governance/management-groups/manage#moving-management-groups-and-subscriptions).

## **Recommended Documents**

- [Management groups move operation permissions](https://docs.microsoft.com/azure/governance/management-groups/overview#moving-management-groups-and-subscriptions)
- [Organize your resources with Azure management groups](https://docs.microsoft.com/azure/governance/management-groups/overview)
- [How to change, delete, or manage your management groups](https://docs.microsoft.com/azure/governance/management-groups/manage)
- [Create management groups to organize Azure resources](https://docs.microsoft.com/azure/governance/management-groups/create)
