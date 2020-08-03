<properties
    pageTitle="I am unable to install the mobility service agent due to other errors"
    description="Questions or issues related to mobility agent installation failure"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744986"
    resourceTags=""
    productPesIds="13670"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e3784e38-589f-4fb2-aa20-360ea40fc5a3"
/>

# I am unable to install the mobility service agent due to other errors

## Unsupported OS/kernel

Check the support matrix to identify the supported versions:

- [Support matrix for disaster recovery of VMware VMs and physical servers to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#replicated-machines(V2A))
- [Support matrix for Azure VM disaster recovery between Azure regions](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#replicated-machine-operating-systems(A2A))

## Prerequisites for success

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

## Mobility agent installation failure

Troubleshooting guidance to resolve most commonly seen installation failures because of connectivity errors.

### Azure to Azure DR

- Resolve connectivity errors with [ids: 151037, 151072, 151195, 151196)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity)
- Set up NSG to whitelist specific URLs for [communication with Azure services](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#example-nsg-configuration)

### VMware to Azure DR

- Ensure all network requirements are met on configuration server to allow [communication with Azure services](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#network-requirements)
- Resolve connectivity errors with [ids: 95117, 95118, 95523, 95105, 95106](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#connectivity-failure-errorid-95117--97118)
- Ensure necessary folders are excluded from anti-virus to avoid [communication blockers](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program)
- Ensure process server is connected & source machine is able to [communicate with process server](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-connectivity-and-replication)

### Mobility agent installation failed due to extension error? Follow the below troubleshooting guidance to resolve most commonly seen errors

- Resolve update failure from Azure Site Recovery extension [time-out error](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#azure-site-recovery-extension-time-out)
- Resolve update failure from VM agent [unresponsive error](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#protection-fails-because-the-vm-agent-is-unresponsive)
- Resolve agent update failure from site recovery extension [update or load errors](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#the-site-recovery-extension-fails-to-update-or-load)
- Resolve extension failure by re-running the extension of VM through [simple powershell command](https://docs.microsoft.com/azure/virtual-machines/extensions/troubleshoot#rerun-the-extension-on-the-vm)
