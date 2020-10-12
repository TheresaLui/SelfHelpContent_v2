<properties
  pagetitle="Azure Stack capacity"
  description="Capacity"
  service="microsoft.azurestack"
  resource="azurestack"
  authors="alexsmithMSFT"
  ms.author="alexsmit,justinha"
  displayorder=""
  selfhelptype="Generic"
  supporttopicids=""
  resourcetags=""
  productpesids="16226"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a87b40e7-27ac-42ad-9541-9dc665013831"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Capacity

Azure Stack Hub allows cloud operators to monitor and manage the compute and storage capacity of their Azure Stack Hub environment. This includes:

* Infrastructure storage
* Tenant virtual machine storage
* Storage backing the blobs, tables, and queues of the Azure Consistent Storage (ACS) services

## **Recommended Steps**

1. Monitor the available storage and memory to ensure sufficient capacity is maintained
2. [Manage storage capacity](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares#manage-available-spaces) to prevent the storage shares from running out of capacity, including:

    - Reclaim capacity from deleted VMs
    - Migrate a container between volumes

3. [Manage physical memory capacity](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity) to ensure there is enough for tenant VM deployments
4. To increase the total available memory capacity for Azure Stack, you can add additional memory to as a scale unit node by working with your hardware vendor (**Note:** All scale nodes that are members of a single scale unit must have the same amount of memory)

## **Recommended Documents**

* [Azure Stack storage capacity planning](https://docs.microsoft.com/azure/azure-stack/capacity-planning-storage)
* [Manage storage capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares)
* [Manage physical memory capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-physical-memory-capacity)
* [Add additional scale unit nodes in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-scale-node)
* [Manage compute capacity for Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planning-compute#frequently-asked-questions)