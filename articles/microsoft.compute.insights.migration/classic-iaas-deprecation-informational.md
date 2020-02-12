<properties
    pageTitle="Classic IaaS Deprecation Information"
    description="Your subscription contains classic IaaS resources that should be migrated to ARM."
    infoBubbleText="Your subscription contains classic IaaS resources that should be migrated to ARM."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="existing-iaas-resources-need-migration"
    diagnosticScenario="classiciaasmigration"
    selfHelpType="diagnostics"
    supportTopicIds="32513964"
    resourceTags="windows,linux"
    productPesIds="14749,15571,15797,16454,16470"
    cloudEnvironments="public,fairfax"
/>

# Classic IaaS VM Deprecation & Migration

<!--issueDescription-->
We have detected that you have classic IaaS VMs in Azure Service Manager (ASM). In 2014, we launched IaaS on Azure Resource Manager (ARM), and have been enhancing capabilities ever since. Because it replaces IaaS resources from ASM, classic IaaS VMs will be retired on 3/1/2023. 
<!--/issueDescription-->

### **How does this affect me?** 
Beginning 3/1/2023, you will no longer be able to start any Classic IaaS VMs using ASM. Any remaining Classic IaaS VMs in a running or stopped-allocated state will be moved to a stopped-deallocated state. 

We will not immediately delete any remaining classic IaaS VMs. After 3/1/2023, we will notify remaining subscriptions who have not migrated their resources about our timelines to delete remaining Classic IaaS VMs. 

The following Azure services and functionality will **NOT** be impacted by this retirement: 
* Cloud Services
* Storage accounts NOT used by Classic IaaS VMs
* Virtual networks (VNets) NOT used by Classic IaaS VMs 

## **Recommended Steps**
 
You should start planning the migration of your existing Classic IaaS VMs from ASM to ARM using our [platform supported migration](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-overview).


## **Recommended Documents**

* [Planning for migration of IaaS resources from classic to Azure Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-plan)
* [Platform-supported migration of IaaS resources from classic to Azure Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-overview)
* [Technical deep dive on platform-supported migration from classic to Azure Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-deep-dive)
* [Migrate IaaS resources from classic to Azure Resource Manager by using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-ps)
* [Common errors during Classic to Azure Resource Manager migration](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-errors)
* [Frequently asked questions about classic to Azure Resource Manager migration](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-faq)