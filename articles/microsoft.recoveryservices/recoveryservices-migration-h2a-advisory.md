<properties
    pageTitle="Site Recovery (Hyper-V to Azure) Advisory"
    description="Site Recovery (Hyper-V to Azure to Azure) Advisory"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang,genlin,TobyTu"
    ms.author="genli"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680611"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="74842b51-f522-4acb-9ef4-f78c5e87ec25"
	ownershipId="Compute_SiteRecovery"
/>

# Advisory questions - Replicate Hyper-V VMs to Azure

**Prerequisites**

* [Supported scenarios and requirements](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-support-matrix) for replicating Hyper-V VMs to Azure
* Run [Deployment planner](https://docs.microsoft.com/azure/site-recovery/hyper-v-deployment-planner-overview) for capacity planning, and to check whether your network bandwidth and storage allocations are sufficient for the amount of churn in your VMs
* [Azure Site Recovery Pricing](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#pricing)

## **Recommended Steps**

The following tutorial series show you how to set up disaster recovery for on-premises VMs:

1. [Prepare Azure resources for disaster recovery of on-premises machines](https://docs.microsoft.com/azure/site-recovery/tutorial-prepare-azure)  
2. [Prepare on-premises Hyper-V servers for disaster recovery to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-prepare-on-premises-tutorial)
3. [Set up replication for Hyper-V VMs](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-tutorial) or  [Hyper-V VMs in VMM clouds](https://docs.microsoft.com/azure/site-recovery/hyper-v-vmm-azure-tutorial)
4. [Run a disaster recovery drill to Azure](https://docs.microsoft.com/azure/site-recovery/tutorial-dr-drill-azure)
5. [Fail over and fail back Hyper-V VMs replicated to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-failover-failback-tutorial)

## **Recommended Documents**

* Replicate specific [Workloads or applications](https://docs.microsoft.com/azure/site-recovery/site-recovery-workload#workload-summary) with Azure Site Recovery 
* [Replicate VMs to Azure using ExpressRoute](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#can-i-use-expressroute-to-replicate-virtual-machines-to-azure)
* [FAQ on replicating Hyper-V VMs to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-common-questions)
