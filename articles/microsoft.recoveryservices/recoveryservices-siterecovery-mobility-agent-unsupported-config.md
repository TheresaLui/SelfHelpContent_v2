<properties
    pageTitle="I am unable to install the mobility service agent due to unsupported configuration or OS"
    description="Questions or issues related to unsupported configurations like disk size, file system, LVM, OS, or distros"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744987"
    resourceTags=""
    productPesIds="16370"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="136642ac-8fb9-412a-8109-61445f30086c"
/>

# I am unable to install the mobility service agent due to unsupported configuration or OS

## **Recommended Steps**

### Unsupported OS/kernel

Check the support matrix to identify the supported versions:

- [Support matrix for disaster recovery of VMware VMs and physical servers to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#replicated-machines(V2A))
- [Support matrix for Azure VM disaster recovery between Azure regions](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#replicated-machine-operating-systems(A2A))

### Prerequisites for success

Avoid failures from unsupported configurations by verifying that you are within our support matrix.

- Supported file systems and storage, such as NFS, LVM, or BTRS:

  - [VMware to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#linux-file-systemsguest-storage)
  - [Azure to Azure](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#replicated-machines---linux-file-systemguest-storage)
  
- Supported disk size & configuration such as dynamic disks, or managed disk:

  - [VMware to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#storage)
  - [Azure to Azure](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#replicated-machines---storage)

- Supported networking configurations such as express route, proxy, NSG, or Load balancer:

  - [VMware to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#network)
  - [Azure to Azure](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#replicated-machines---networking)
