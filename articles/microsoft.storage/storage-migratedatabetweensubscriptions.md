<properties
	pageTitle="Move Data Between Subscriptions"
	description="Move Data Between Subscriptions"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602699"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
/>

# Move Resources Between RG or Subscription

## **Recommended steps**

**Call support when you need to**<br>
- Move your resources to a new Azure account (and [Active Directory tenant](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move)).<br>
- Move classic resources but are having trouble with the [limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations).<br>

**Move Resources Between RG or Subscription**<br>
- Move Resource Manager resources.<br>
- Move classic resources according to the [classic deployment limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)<br>

There are some important steps to perform before moving a resource. By verifying these conditions, you can avoid errors.

1. The service must enable the ability to move resources. See the list below for information about which [services enable moving resources](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move).
2. The source and destination subscriptions must exist within the same [Active Directory tenant](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move). To move to a new tenant, call support.
3. The destination subscription must be registered for the resource provider of the resource being moved. If not, you receive an error stating that the subscription is not registered for a resource type. You might encounter this problem when moving a resource to a new subscription, but that subscription has never been used with that resource type. To learn how to check the registration status and register resource providers, see [Resource providers and types](https://azure.microsoft.com/documentation/articles/resource-manager-supported-services/#resource-providers-and-types).
4. If you are moving App Service app, you have reviewed [App Service limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#app-service-limitations).
5. If you are moving resources associated with Recovery Services, you have reviewed the [Recovery Services limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#recovery-services-limitations).
6. If you are moving resources deployed through classic model, you have reviewed [Classic deployment limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations).

## **Recommended documents**
[Move Resources to New Resource Group or Subscription](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/)
