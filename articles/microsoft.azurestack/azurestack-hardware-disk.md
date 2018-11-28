<properties
    pageTitle="Azure Stack disks"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567931,32629241"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack disks

As a cloud operator, you have a limited amount of storage to work with. The amount of storage is defined by the solution you implement. Your solution is provided by your OEM vendor when you use a multi-node solution.<br>

When a share is 100% utilized, the storage service no longer functions for that share.<br>

## **Recommended steps**

1. Monitor the available storage to ensure efficient operations are maintained.<br>
2. Plan to manage space to prevent the shares from running out of capacity.<br>
    Options to manage capacity include:<br>
    - Reclaim capacity<br>
    - Migrate a container<br>
3. To increase the total available memory capacity for Azure Stack, you can add additional memory. In Azure Stack your physical server is also referred to as a scale unit node. All scale unit nodes that are members of a single scale unit must have the same amount of memory. For more information, see [Manage physical memory capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity).<br>

## **Recommended documents**

[Manage storage capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares)<br>
[Add additional scale unit nodes in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-scale-node)<br>
[Manage physical memory capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity)