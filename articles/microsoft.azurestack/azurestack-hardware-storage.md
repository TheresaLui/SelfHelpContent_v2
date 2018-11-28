<properties
    pageTitle="Azure Stack storage devices"
    description=""
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

# Azure Stack storage

The hyper-converged configuration of Azure Stack allows for the sharing of physical storage devices. The three main divisions of the available storage are between the infrastructure, temporary storage of the tenant virtual machines, and the storage backing the blobs, tables, and queues of the Azure Consistent Storage (ACS) services.<br>

There is storage capacity used for the operating system, local logging, dumps, and other temporary infrastructure storage needs. This local storage capacity is separate (devices and capacity) from the storage devices brought under management of the Storage Spaces Direct configuration. The remainder of the storage devices is placed in a single pool of storage capacity regardless of the number of servers in the Scale Unit.

## **Recommended steps**

1. Monitor the available storage to ensure efficient operations are maintained<br>
2. Plan to manage space to prevent the shares from running out of capacity<br>
    Options to manage capacity include:<br>
    - Reclaim capacity<br>
    - Migrate a container<br>
3. To increase the total available memory capacity for Azure Stack, you can add additional memory. In Azure Stack your physical server is also referred to as a scale unit node. All scale unit nodes that are members of a single scale unit must have the same amount of memory.

## **Recommended documents**

[Azure Stack storage capacity planning](https://docs.microsoft.com/azure/azure-stack/capacity-planning-storage)<br>
[Manage storage capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares)<br>
[Add additional scale unit nodes in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-scale-node)<br>
[Manage physical memory capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity)