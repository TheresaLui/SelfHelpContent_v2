<properties
  pagetitle="Moving Data Factory across resource groups, subscriptions or tenants"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="susabat,haoc"
  selfhelptype="Generic"
  supporttopicids="32781331"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  articleid="afaa0da1-5863-4d2d-af5f-2b3db82b3ef7"
  ownershipid="AzureData_DataFactory" />
# Moving Data Factory across resource groups, subscriptions or tenants

Most users are able to resolve issues concerning moving a data factory across resource groups, subscriptions, or tenants by using the following steps.

## **Recommended Steps**

1. To copy or clone a data factory, follow [these directions](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory)

2. If you've moved Data Factory from one tenant to another, and are now running into issues, try to generate a new managed identity to resolve it. You can use Powershell or the REST API, as described in [Generate service identity](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-service-identity).

## **Recommended Documents**

* [Move resources to a new resource group or subscription](https://docs.microsoft.com/ azure/azure-resource-manager/management/move-resource-group-and-subscription)
* [Best Practices to Move Data Pipelines]( https://social.msdn.microsoft.com/Forums/e952327e-43cf-4e9f-ae01-068a836fed81/best-practice-to-move-pipelines-to-different-data-factory?forum=AzureDataFactory)
* [Migrate Data Pipelines]( https://www.linkedin.com/pulse/migrate-data-pipelines-among-different-azure-factories-himanshu-rathi/?articleId=6691596315345924096)
