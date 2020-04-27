<properties
	pageTitle="Site Recovery (System Center VMM to Azure) Advisory"
	description="Site Recovery (System Center VMM to Azure) Advisory"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang,genlin"
    ms.author="asgang,genli"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630517"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="ea223e91-ca3d-432b-b10c-48e784c66cda"
	ownershipId="Compute_SiteRecovery"
/>

# Advisory questions - Replicate Hyper-V VMs managed by System Center VVM to Azure

**Prerequisites**

- [Supported scenarios and requirements](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-support-matrix)
 for replicating Hyper-V VMs to Azure
- Run [Deployment planner](https://docs.microsoft.com/azure/site-recovery/hyper-v-deployment-planner-overview) for capacity planning, and check whether your network bandwidth and storage allocations are sufficient for the amount of churn in your VMs
- [Azure Site Recovery Pricing](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#pricing)

## **Recommended Documents**

The following tutorial series show you how to set up disaster recovery for on-premises VMs:

1. [Prepare Azure resources for disaster recovery of on-premises machines](https://docs.microsoft.com/azure/site-recovery/tutorial-prepare-azure)  
2. [Prepare on-premises Hyper-V servers for disaster recovery to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-prepare-on-premises-tutorial)
3. [Set up replication for Hyper-V VMs in System Center VVM](https://docs.microsoft.com/azure/site-recovery/hyper-v-vmm-azure-tutorial)
4. [Run a disaster recovery drill to Azure](https://docs.microsoft.com/azure/site-recovery/tutorial-dr-drill-azure)
5. [Failover and failback Hyper-V VMs replicated to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-failover-failback-tutorial)

**Additional Information**

* Replicate specific [Workloads or applications](https://docs.microsoft.com/azure/site-recovery/site-recovery-workload#workload-summary) with Azure Site Recovery 
* [Replicate VMs to Azure using ExpressRoute](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#can-i-use-expressroute-to-replicate-virtual-machines-to-azure) 
* [FAQ on replicating Hyper-V VMs to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-common-questions)
