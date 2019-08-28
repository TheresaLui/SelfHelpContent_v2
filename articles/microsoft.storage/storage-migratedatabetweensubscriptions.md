<properties
	pageTitle="Move Data Between Subscriptions"
	description="Move Data Between Subscriptions"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	ms.author="raprasad"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602699"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
	articleId="f2be20c0-4a8e-4926-a468-ba823f86d27c"
/>

# Move Resources Between RG or Subscription

## **Recommended Steps**

1. Call support for assistance with:
	* Moving your resources to a new Azure account (and [Active Directory tenant](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move))
	* Moving classic resources and experiencing issues with [limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)
	* Moving Resource Manager resources
	* Moving classic resources according to the [classic deployment limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)<br>

There are some important steps to perform before moving a resource. By verifying these conditions, you can avoid errors.

1. The service must enable the ability to move resources. See the list below for information about which [services enable moving resources](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move).
2. The source and destination subscriptions must exist within the same [Active Directory tenant](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move). To move to a new tenant, call support.
3. The destination subscription must be registered for the resource provider of the resource being moved. If not, you receive an error stating that the subscription is not registered for a resource type. You might encounter this problem when moving a resource to a new subscription, but that subscription has never been used with that resource type. To learn how to check the registration status and register resource providers, see [Resource providers and types](https://azure.microsoft.com/documentation/articles/resource-manager-supported-services/#resource-providers-and-types).
4. If you are moving the App Service app, review the [App Service limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#app-service-limitations)
5. If you are moving resources associated with Recovery Services, review the [Recovery Services limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#recovery-services-limitations)
6. If you are moving resources deployed through the classic model, review the [Classic deployment limitations](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)

## **Recommended Documents**

- [Move Resources to New Resource Group or Subscription](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/)<br>
- [Data transfer for large datasets with low or no network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network)<br>
- [Data transfer for small datasets with low to moderate network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-small-dataset-low-moderate-network)<br>
- [Data transfer for large datasets with moderate to high network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-moderate-high-network)<br>
- [Solutions for periodic data transfer](https://docs.microsoft.com/azure/storage/common/storage-solution-periodic-data-transfer)<br>
