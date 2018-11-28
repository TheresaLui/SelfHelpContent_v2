<properties
    pageTitle="Azure Stack storage devices"
    description="Storage Capacity"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567943,32629224,32629260"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack Storage Capacity

The hyper-converged configuration of Azure Stack allows for the sharing of physical storage devices. The three main divisions of the available storage are between:

* Infrastructure storage
* Tenant virtual machine storage
* Storage backing the blobs, tables, and queues of the Azure Consistent Storage (ACS) services

## **Recommended steps**

1. Monitor the available storage to ensure efficient operations are maintained
2. Plan to manage space to prevent the shares from running out of capacity<br>
    Options to manage capacity include:
    - Reclaim capacity
    - Migrate a container
3. To increase the total available memory capacity for Azure Stack, you can add additional memory. In Azure Stack your physical server is also referred to as a scale unit node. All scale unit nodes that are members of a single scale unit must have the same amount of memory.

## **Recommended documents**

[Azure Stack storage capacity planning](https://docs.microsoft.com/azure/azure-stack/capacity-planning-storage)<br>
[Manage storage capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares)<br>
[Manage physical memory capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity)<br>
[Add additional scale unit nodes in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-scale-node)
