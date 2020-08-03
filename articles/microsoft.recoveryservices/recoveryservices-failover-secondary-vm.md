<properties
    pageTitle="I am having issues with the secondary VM after successful failover"
    description="Questions or issues related to booting up the secondary VM, accessing it, etc. post failover"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744981"
    resourceTags=""
    productPesIds="13670"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dd97631c-d041-461b-850c-745229af70e8"
/>

# I am having issues with the secondary VM after successful failover

## **Recommended Documents**

- [Connect to a VM after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)
- [Connect button grayed out on VM](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#unable-to-connectrdpssh-to-the-failed-over-virtual-machine-due-to-grayed-out-connect-button-on-the-virtual-machine)
- [How to troubleshoot RDP connection to Windows VM?](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
- [How to troubleshoot SSH connection to Linux VM?](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-ssh-connection)
- [How to assign New IP address to a VM after failover](https://docs.microsoft.com/archive/blogs/srinathv/how-to-add-a-public-ip-address-to-azure-vm-for-vm-failed-over-using-asr)
- [How to retain fixed private IP address while failing over to Azure](https://docs.microsoft.com/azure/site-recovery/concepts-on-premises-to-azure-networking#retaining-ip-addresses)
- [Insufficient cores available to failover? Follow these steps to increase the quota](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests)
- [The selected target location is not enabled for VM creation in your subscription. Change location or follow these instructions to enable VM creation](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors)
- [Troubleshooting Failover error codes with: Error ID 28031, Error ID 28092, Error ID 70038](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot)
- [Orchestrate failover with recovery plans and run automation scripts as part of failover](https://github.com/Azure/azure-quickstart-templates/tree/master/asr-automation-recovery/scripts)
- [Script to assign public IP address to failed over VM](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-AddPublicIp.ps1)
- [Script to update DNS records of the VM being failed over](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-DNS-UpdateIP.ps1)
