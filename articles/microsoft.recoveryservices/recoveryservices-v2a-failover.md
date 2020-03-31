<properties
	pageTitle="Site Recovery (VMware to Azure)/Failover: Unplanned failover"
	description="Site Recovery (VMware to Azure)/Failover: Unplanned failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="prateek9us"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536465"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax"
	articleId="c3c4fe90-cda5-477c-bbff-c0e987f454bc"
	ownershipId="Compute_SiteRecovery"
/>

# Run a Failover in Site recovery - VMware to Azure
## **Recommended steps**

- Not enough **cores** available to failover? [Follow these steps to increase the quota ](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)<br>
- How to [**failover** to Azure (step-by-step)](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover) and [**connect to VM** after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)<br>
- [How to **retain fixed private IP address** while failing over to Azure](https://docs.microsoft.com/azure/site-recovery/concepts-on-premises-to-azure-networking#retaining-ip-addresses)<br>
- [How to **preserve the drive letters** of data disks when failing over to Azure](https://support.microsoft.com/help/3031135/how-to-preserve-the-drive-letter-for-protected-virtual-machines-that-a)<br>
- [VM **Connect button** grayed out?](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#unable-to-connectrdpssh-to-the-failed-over-virtual-machine-due-to-grayed-out-connect-button-on-the-virtual-machine) Or [**unable to RDP/SSH** to VM?](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#unable-to-connectrdpssh-to-the-failed-over-virtual-machine-even-though-connect-button-is-available-not-grayed-out-on-the-virtual-machine)<br>
- [Orchestrate failover with recovery plans](https://docs.microsoft.com/azure/site-recovery/site-recovery-create-recovery-plans) and [run automation scripts as part of failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-runbook-automation)<br>
- Troubleshoot [RDP connection to Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection) and [SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)<br>
- Troubleshoot Failover error codes with: [Error ID 28031](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28031), [Error ID 28092](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28092), [Error ID 70038](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-70038)<br>


## **Recommended documents**

**Automation**<br>

- [Sample scripts to Automate different operations during failover](https://github.com/Azure/azure-quickstart-templates/tree/master/asr-automation-recovery/scripts)<br>
- [Script to assign public IP address to failed over VM](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-AddPublicIp.ps1)<br>
- [Script to update DNS records of the VM being failed over](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-DNS-UpdateIP.ps1)<br>

**Test Failover**<br>

- [How to Run a Test Failover to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure)<br>
- [Create a network for test failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#create-a-network-for-test-failover)<br>
- [Test failover considerations to failover the VM into production recovery network](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#test-failover-to-a-production-network-in-the-recovery-site)<br>
- [Add a public IP address to the VM after test failover](https://aka.ms/addpublicip)<br>

**Failback**<br>

- [How to failback from Azure to On-premises VMware site (step-by-step)](https://docs.microsoft.com/azure/site-recovery/site-recovery-how-to-failback-azure-to-vmware)<br>

**Protect AD DNS**<br>

- [Protect Active Directory and DNS](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory)<br>
