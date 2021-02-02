<properties
  pagetitle="Data Factory Limits&#xD;"
  description="Raise limits for Data Factory V2"
  ms.author="chez,susabat"
  selfhelptype="Generic"
  supporttopicids="32781330"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="4bb334b2-7454-45d4-aeb3-ef85910ef76d"
  ownershipid="AzureData_DataFactory" />
# Data Factory Limits


Azure Data Factory is a multitenant service that has the following default limits in place to make sure customer subscriptions are protected from each other's workloads. To raise the limits up to the maximum for your subscription, you may contact support. In our experience, you can optimize your pipelines to stay below the limits.

## **Recommended Steps**

- Review Azure Data Factory Limits at [Data Fcatory Limits](https://github.com/MicrosoftDocs/azure-docs/blob/master/includes/azure-data-factory-limits.md)
- Some default limits can be increased per [Customer Request](https://azure.microsoft.com/blog/azure-limits-quotas-increase-requests/) 
- However, some limits, including bytes per object for pipeline objects, cannot be increased above the default. 
- See the following documentation link for up-to-date information.
- If you hit the bytes per object for pipeline objects limit, we recommend that  you split the pipeline into several smaller pipelines.

## **Recommended Documents**

- [Data Factory Limits (see Version 2 section)](https://docs.microsoft.com/azure/azure-subscription-service-limits#data-factory-limits)
- [Azure Service Limits](https://docs.microsoft.com/azure/azure-resource-manager/management/azure-subscription-service-limits)