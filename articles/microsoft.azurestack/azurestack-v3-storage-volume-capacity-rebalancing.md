<properties
    pageTitle="Azure Stack volume capacity and re-balancing"
    description="Azure Stack volume capacity and re-balancing"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663921"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="92d85eb7-cd78-434f-96fe-8292931b29d6"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Volume capacity and rebalancing

## **Recommended Documents**

Azure Stack cloud operators monitor and manage the storage capacity of their Azure Stack deployment. The Azure Stack storage infrastructure allocates a subset of the total storage capacity of the Azure Stack deployment, to be used for storage services. The storage services store a tenant's data in shares on volumes that correspond to the nodes of the deployment.

- [Overview of Azure Stack capacity planning](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planning-overview)
- [Azure Stack Capacity Planner](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planner)
- [Azure Stack memory](https://docs.microsoft.com/azure-stack/operator/azure-stack-capacity-planning-compute#azure-stack-memory)
- [Monitoring shares](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-storage-shares#monitor-shares)
- [Manage available space](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-storage-shares#manage-available-space)
- [Azure Stack storage: Differences and considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-acs-differences)

