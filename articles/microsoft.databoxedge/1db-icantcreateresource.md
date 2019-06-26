<properties
    pageTitle="I can't create a Data Box Edge resource"
    description="I can't create a Data Box Edge resource"
    service="microsoft.databoxedge"
    resource="databoxedgedevices"
    authors="anoobbacker"
    ms.author="anbacker"
    authoralias="anbacker"
    displayOrder="10"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="DataBoxEdge"
    productPesIds=""
    cloudEnvironments="public"
    articleId="64258305-b205-46e8-8168-f796dcf0de1a"
/>

# I can't create a Data Box Edge resource

## **Recommended Steps**

If you can't create a Data Box Edge resource, do the following:

1. Ensure that you have permissions as a contributor or higher at a resource group level.
2. Resource providers are registered on the level of the subscription. By default, any new Azure subscription is pre-registered with a list of commonly used resource providers. The resource provider for _Microsoft.DataBoxEdge_ is not included in this list. You need the resource providers to be registered. For more information, go to [Manage resource access permissions](https://docs.microsoft.com/azure/databox-online/data-box-edge-manage-access-power-connectivity-mode#manage-resource-access)
3. You should have a _User_ access on Active Directory tenant as you need to be able to _Read all directory objects_. You can't be a Guest user as they don't have permissions to _Read all directory objects_. If you're a guest, then the operations such as generation of an activation key, creation of a share on your Data Box Edge device, creation of a user will all fail. For more information, go to [Default access for administrators, users, and guest users](https://docs.microsoft.com/previous-versions/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes#default-access-for-administrators-users-and-guest-users-).
4. If you've already created the resource, wait until your request is approved. Once the device is ready for allocation, Microsoft contacts you via the email used for notification.

## **Recommended Documents**

* [Manage resource access permissions](https://docs.microsoft.com/azure/databox-online/data-box-edge-manage-access-power-connectivity-mode#manage-resource-access)
