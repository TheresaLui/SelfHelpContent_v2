<properties
    pageTitle="Azure Stack storage devices"
    description="Storage Capacity"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    authorAlias="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629224,32629260"
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

1. Monitor the available storage and memory to ensure sufficient capacity is maintained
2. [Manage storage capacity](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares) to prevent the storage shares from running out of capacity<br>
    Options to manage capacity include:
    - Reclaim capacity
    - Migrate a container
3. [Manage physical memory capacity](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity) to ensure there is enough for tenant VM deployments<br>
4. To increase the total available memory capacity for Azure Stack, you can add additional memory to as a scale unit node by working with your hardware vendor<br>
**Note:** All scale nodes that are members of a single scale unit must have the same amount of memory.

## **Recommended documents**

[Azure Stack storage capacity planning](https://docs.microsoft.com/azure/azure-stack/capacity-planning-storage)<br>
[Manage storage capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares)<br>
[Manage physical memory capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity)<br>
[Add additional scale unit nodes in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-scale-node)
