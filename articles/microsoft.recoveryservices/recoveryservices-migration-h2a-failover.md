<properties
    pageTitle="Site Recovery (Hyper-V Site to Azure)/Failover: Planned and unplanned failover"
    description="Site Recovery (Hyper-V Site to Azure)/Failover: Planned and unplanned failover"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="prateek9us,TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680609"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="77842b51-f522-4acb-9ef4-f78c5e87ec25"
	ownershipId="Compute_SiteRecovery"
/>

# Run a Failover in Site recovery - Hyper-V to Azure

## **Recommended Steps**

- [How to **failover** a Hyper-V VM to Azure (step-by-step)](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover)
- [How to **retain fixed IP address** while failing over to Azure](https://docs.microsoft.com/azure/site-recovery/concepts-on-premises-to-azure-networking#retaining-ip-addresses)
- [How to **assign new IP address** to a VM after failover](https://azure.microsoft.com/blog/networking-infrastructure-setup-for-microsoft-azure-as-a-disaster-recovery-site/)
- [How to **preserve the drive letters** of data disks when failed over to Azure](https://support.microsoft.com/help/3031135/how-to-preserve-the-drive-letter-for-protected-virtual-machines-that-a)
- [How to **connect to VM** after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)
- [Issue] [*Connect button grayed out on VM*](https://blogs.technet.microsoft.com/srinathv/2018/02/07/unable-to-connectrdpssh-to-the-failed-over-vm-using-azure-site-recovery/)
- [Issue] [*Connect button available and unable to RDP/SSH to VM*](https://blogs.technet.microsoft.com/srinathv/2018/02/07/unable-to-connectrdpssh-to-the-failed-over-vm-using-azure-site-recovery/)
- [How to] [troubleshoot RDP connection to Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)
- [How to] [troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)
- [Issue] [*There aren't sufficient cores available to failover* Follow these steps to increase the quota](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)
- [Issue] [*The selected target location is not enabled for VM creation in your subscription.* Change location or follow these instructions to enable VM creation](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)
- [Issue] Troubleshooting Failover error codes with: [Error ID 28031](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28031), [Error ID 28092](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28092), [Error ID 70038](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-70038)

## **Recommended Documents**

### Automation

- How to customize recovery plan to run automation scripts as part of failover [Add Azure Automation runbooks to recovery plans](https://docs.microsoft.com/azure/site-recovery/site-recovery-runbook-automation)
- [Sample scripts to Automate different operations during failover](https://github.com/Azure/azure-quickstart-templates/tree/master/asr-automation-recovery/scripts)
- [Script to assign public IP address to failed over VM](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-AddPublicIp.ps1)
- [Script to update DNS records of the VM being failed over](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-DNS-UpdateIP.ps1)

### Test Failover

- [How to Run a Test Failover to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure)
- [Create a network for test failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#create-a-network-for-test-failover)
- [Test failover considerations to **Failover the VM into your production network**](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#test-failover-to-a-production-network-in-the-recovery-site)
- [How to run a test failover for a single VM](https://docs.microsoft.com/azure/site-recovery/tutorial-dr-drill-azure#verify-vm-properties)
- [Add a public IP address to the VM after test failover](https://blogs.technet.microsoft.com/srinathv/2018/02/07/how-to-add-a-public-ip-address-to-azure-vm-for-vm-failed-over-using-asr/)

### Failback

- [Step by step instruction on how to failback from Azure to On-premises Hyper-V site](https://docs.microsoft.com/azure/site-recovery/site-recovery-failback-from-azure-to-hyper-v)

### Protect AD DNS

- [Protect Active Directory and DNS](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory)
