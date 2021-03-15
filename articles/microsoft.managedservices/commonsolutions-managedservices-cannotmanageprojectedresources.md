<properties
  pagetitle="Cannot manage projected resources"
  description="Cannot manage projected resources"
  service=""
  resource=""
  ms.author="prukulka,sezhen"
  selfhelptype="Generic"
  supporttopicids="32642165"
  resourcetags=""
  productpesids="16761"
  cloudenvironments="fairfax,mooncake,public,usnat,ussec,blackforest"
  disableclouds=""
  articleid="commonsolutions-managedservices-cannotmanageprojectedresources"
  ownershipid="Compute_AzureLighthouse" />
# Cannot manage projected resources

Most users are able to manage projected resources using the following steps.

## **Recommended Steps**

**Do you have the appropriate delegated permissions?**

As a user, make sure that you’re 1) part of the group or users that have been granted access to the resources, and 2) that the appropriate [RBAC role](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles) has been assigned. 

For example, if you’d like to see a customer delegation, then you must have the Reader role. Or, if you’d like to remove a customer delegation, then you must have the Managed Service Registration Assignment Delete Role.

You can [check your assigned permissions](https://docs.microsoft.com/azure/lighthouse/how-to/view-manage-customers#view-and-manage-delegations) on the "My Customers" blade in Azure Portal.

**Have you selected the correct scope?**

If you’re in the Azure Portal, check your [global and local filters](https://docs.microsoft.com/azure/lighthouse/how-to/view-manage-customers#work-in-the-context-of-a-delegated-subscription) to select a specific scope or select all.

**Are you trying something that’s not supported by Azure Lighthouse?**

Be aware of [current limitations](https://docs.microsoft.com/azure/lighthouse/concepts/cross-tenant-management-experience#current-limitations). 

## **Recommended Documents**

* [View and manage customers and delegated resources](https://docs.microsoft.com/azure/lighthouse/how-to/view-manage-customers)
