<properties
	pageTitle="Site Recovery (Hyper-V Site to Azure)/Failover: Test failover"
	description="Site Recovery (Hyper-V Site to Azure)/Failover: Test failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="prateek9us"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536460"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="adb2554b-39d8-4f4d-9d86-6879e1914848"
	ownershipId="Compute_SiteRecovery"
/>

# Run a test failover in Site recovery - Hyper-V to Azure
## **Recommended steps**

- [How to Run a **Test Failover** to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure)<br>
- [How to Create a **network for test failover**](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#create-a-network-for-test-failover)<br>
- [Test failover considerations to **Failover the VM into your production network**](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#test-failover-to-a-production-network-in-the-recovery-site)<br>
- [How to run a **test failover for a single VM?**](https://docs.microsoft.com/azure/site-recovery/tutorial-dr-drill-azure#verify-vm-properties)<br>
- [Test failover **considerations for Active Directory** to run a **failover for application testing**](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory#test-failover-considerations)<br>
- [How to **connect to VM** after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)<br>
- [**Add a public IP address** to the VM after test failover](https://aka.ms/addpublicip)<br>
- [Issue] [*Connect button grayed out on VM*](https://aka.ms/unabletordpssh)<br>
- [Issue] [*Connect button available and unable to RDP/SSH to VM*](https://aka.ms/unabletordpssh)<br>
- [How to] [troubleshoot RDP connection to Windows VM?](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)<br>
- [How to] [troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)<br>
- [Issue] [*There aren't sufficient cores available to failover?* Follow these steps to increase the quota ](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)<br>
- [Issue] [*The selected target location is not enabled for VM creation in your subscription.* Change location or follow these instructions to enable VM creation ](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)<br>
- [Issue] Troubleshooting Failover error codes with: [Error ID 28031](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28031), [Error ID 28092](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28092), [Error ID 70038](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-70038)<br>

**Active directory and DNS**<br>
- [Issue] [VM-Generation ID has changed post Failover?](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory#issues-caused-by-virtualization-safeguards)<br>
- [Issue] [Invocation ID has changed post failover?](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory#issues-caused-by-virtualization-safeguards)<br>
- [Issue] [Sysvol and Netlogon shares are not available post failover?]((https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory#issues-caused-by-virtualization-safeguards)<br>
- [Issue] [Unable to find DFSR databases post failover?](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory#issues-caused-by-virtualization-safeguards)<br>
- [Issue] [How to troubleshoot domain controller issues during test failover?](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory#troubleshoot-domain-controller-issues-during-test-failover)<br>


## **Recommended documents**

**Automation**<br>

- How to customize recovery plan to run automation scripts as part of failover? [Add Azure Automation runbooks to recovery plans ](https://docs.microsoft.com/azure/site-recovery/site-recovery-runbook-automation)<br>
- [Sample scripts to Automate different operations during failover](https://github.com/Azure/azure-quickstart-templates/tree/master/asr-automation-recovery/scripts)<br>
- [Script to assign public IP address to failed over VM](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-AddPublicIp.ps1)<br>
- [Script to update DNS records of the VM being failed over](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-DNS-UpdateIP.ps1)<br>

**Failover**<br>
- [Step by step instruction on how to failover a Hyper-V VM to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover)<br>
- [How to retain the fixed IP address while failing over to Azure](https://docs.microsoft.com/azure/site-recovery/concepts-on-premises-to-azure-networking#retaining-ip-addresses)<br>
- [How to assign New IP address to a VM after failover](https://azure.microsoft.com/blog/networking-infrastructure-setup-for-microsoft-azure-as-a-disaster-recovery-site/)<br>
- [How to preserve the drive letters of data disks when failed over to Azure](https://support.microsoft.com/help/3031135/how-to-preserve-the-drive-letter-for-protected-virtual-machines-that-a)<br>

**Failback**<br>
- [Step by step instruction on how to failback from Azure to On-premises Hyper-V site](https://docs.microsoft.com/azure/site-recovery/site-recovery-failback-from-azure-to-hyper-v)<br>

**Protect AD DNS**<br>

- [Protect Active Directory and DNS](https://docs.microsoft.com/azure/site-recovery/site-recovery-active-directory)<br>
