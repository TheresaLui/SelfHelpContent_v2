<properties
    pageTitle="Troubleshooting Management groups and subscriptions"
    description="Common issues with using management groups and subscriptions"
    service="Microsoft.Management"
    resource="managementgroups"
    authors="rthorn17"
    ms.author="rithorn"
    articleId="managementgroups-problemwithsubscriptions"
    selfHelpType="generic"
    supportTopicIds="32743302,32743301,32743299,32743300"
    productPesIds="16530"
    cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
    ownershipId="ARM_ManagementGroups"
/>

# Management group troubleshooting

Here are a some common issues you might experience with subscriptions and management groups:

- [I received a generic error saying something went wrong and to contact support](#generic-error-when-something-went-wrong)
- [The management group or subscription I want to move is not listed in the drop down](#The-subscription-or-management-group-is-not-listed)
- [I can't see the subscription that I just moved under a management group](#I-cannot-see-the-subscription-that-I-just-moved)
- [Issues with Resource Groups?](#issues-with-Resource-Groups)

## Generic error when something went wrong

Sometimes when an unexpected error happens when moving a subscription or management group within the hierarchy. When this happens you might see a message that says "There has been an error moving the subscription. If the problem continues, please contact support".  

If you are seeing this message there a few items to check prior to submitting a support ticket to help you quickly resolve the issue.  In most cases it is an issue with the permissions you have that happens when moving a subscription or management group.  Use these recommend steps to make sure you have the correct permissions.  

## **Recommended Steps**

1. Go to the subscription, or child management group, you are trying to move and see what permissions you have. To move a child subscription or management group, **you are required to have general write permissions and role assignment write permissions.** An example built in role and most commonly assigned role, is "Owner" as this role has the ability to create/update/delete management groups along with the ability to create and delete User Role Assignments.
1. Check the current parent management group of the subscription or management group you are trying to move for your permissions. To move a subscription or management group, **you need to have write access on the current parent management group.** You should have "Owner", "Contributor", "Management Group Contributor" roles or equivalent custom role on the group.

    * **Exception**: If the current parent management group is the root management group of the hierarchy, the service will not check this permission as this is the default location  

1. Check the target parent management group you are trying to move the subscription or management group to for your permissions. To move a subscription or management group, **you need to have write access on the target parent management group.** You should have "Owner", "Contributor", "Management Group Contributor" roles, or equivalent custom role on the group.

    * **Exception**: If the target parent management group is the root management group of the hierarchy, the service will not check this permission as this is the default location

With these three permissions being true, you will be able to move the subscription or management group between different management groups. For more information see, [How to change, delete, or manage your management groups](https://docs.microsoft.com/azure/governance/management-groups/manage#moving-management-groups-and-subscriptions).

## The subscription or management group is not listed

When working within the Azure portal, the dropdowns will only show you the items you are able to move. This is to help avoid any errors as the service only will present the items with the proper permissions. If you are not seeing the proper items in the dropdowns, check your permissions on the subscriptions or management groups. For help see [Recommended Steps](#recommended-steps) on how to check your permissions.  

## I cannot see the subscription that I just moved

If you are having trouble finding the subscription you just moved under a management group, there are a couple steps you can do to find out what happened:

- Check the notifications section in the portal to see if there was a failure. If the process of moving the subscription failed, you will see an error in the notifications. You can find the notifications window in the upper right hand corner of the Azure portal with the icon of a bell.
- Check the default subscription filter to make sure the subscription you are looking for is enabled in the views. You can find the Directory + subscription filter window in the upper right hand corner of the Azure portal with the icon of a notebook with the filter icon on top of it.
- Check your permission on the new management group and the subscription itself. While you needed the proper permissions to move the subscription there could have been changes to the role assignments since then. See [Recommended Steps](#recommended-steps) on how to check your permissions.

- Was the move done within the last 30 minutes?

  - If so, there could be a user token issue that is preventing the subscription from showing within the Azure portal. Try refreshing the browser and/or logging in and out of the Azure portal. This will renew the user token.
  - If you are on the management group pages within the Azure portal, select the refresh button on the table to refresh the table
  - It could be possible there is a data latency issue with the replications. If you don't see the subscription after 30 minutes then proceed submitting a support request for help.

## Issues with Resource Groups

Management groups are different objects in Azure than resource groups. Resource groups are groupings under the subscription that hold resources directly. Management groups are a grouping construct that are above the subscription level and can only have subscriptions or other management groups as children. For more information on Resource Groups, see [Manage Azure Resource Manager resource groups.](https://docs.microsoft.com/azure/azure-resource-manager/manage-resource-groups-portal).

## **Recommended Documents**

- [Management groups move operation permissions](https://docs.microsoft.com/azure/governance/management-groups/overview#moving-management-groups-and-subscriptions)
- [Organize your resources with Azure management groups](https://docs.microsoft.com/azure/governance/management-groups/overview)
- [How to change, delete, or manage your management groups](https://docs.microsoft.com/azure/governance/management-groups/manage)
- [Create management groups to organize Azure resources](https://docs.microsoft.com/azure/governance/management-groups/create)
