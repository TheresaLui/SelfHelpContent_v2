<properties
  pagetitle="Azure Stack Volume capacity and rebalancing"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="justinha"
  selfhelptype="Generic"
  supporttopicids="32629224,32737308,32741944"
  resourcetags=""
  productpesids="16226,17131,17058"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="92d85eb7-cd78-434f-96fe-8292931b29d6"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Volume capacity and rebalancing

## **Recommended Documents**

We recently updated guidance about different ways to reallocate memory for VMs running in Azure Stack Hub. For more information, see [considerations for memory deallocation](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planning-compute#considerations-for-deallocation).

Azure Stack cloud operators monitor and manage the storage capacity of their Azure Stack deployment. The Azure Stack storage infrastructure allocates a subset of the total storage capacity of the Azure Stack deployment, to be used for storage services. The storage services store a tenant's data in shares on volumes that correspond to the nodes of the deployment.

- [Overview of Azure Stack capacity planning](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planning-overview)
- [Azure Stack Capacity Planner](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planner)
- [Azure Stack memory](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planning-compute#azure-stack-memory)
- [Monitoring shares](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-storage-shares#monitor-shares)
- [Manage available space](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-storage-shares#manage-available-space)
- [Azure Stack storage: Differences and considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-acs-differences)