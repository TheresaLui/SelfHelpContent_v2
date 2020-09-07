<properties
	pageTitle="Site Recovery (VMware to Azure)/Not able to conect to VM after failover"
	description="Site Recovery (VMware to Azure)/Not able to conect to VM after failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="prateek9us"
    ms.author="genli"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32680617"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a7573f50-08c4-4744-8597-84f70800d159"
	ownershipId="Compute_SiteRecovery"
/>

# Unable to connect to VM after failover - VMware to Azure

## **Recommended Steps**

- Prepare to [**connect to VM** after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)<br>
- [VM **Connect button** grayed out?](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#unable-to-connectrdpssh-to-the-failed-over-virtual-machine-due-to-grayed-out-connect-button-on-the-virtual-machine) Or [**unable to RDP/SSH** to VM?](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#unable-to-connectrdpssh-to-the-failed-over-virtual-machine-even-though-connect-button-is-available-not-grayed-out-on-the-virtual-machine)<br>
- Troubleshoot [RDP connection to Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection) and [SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)<br>
- Add Public IP address to a VM [during failover with scripts](https://docs.microsoft.com/azure/site-recovery/site-recovery-runbook-automation) or [after failover](https://blogs.technet.microsoft.com/srinathv/2018/02/07/how-to-add-a-public-ip-address-to-azure-vm-for-vm-failed-over-using-asr/)<br>
- [How to **retain fixed private IP address** while failing over to Azure](https://docs.microsoft.com/azure/site-recovery/concepts-on-premises-to-azure-networking#retaining-ip-addresses)<br>

## **Recommended Documents**

- [Orchestrate failover with recovery plans](https://docs.microsoft.com/azure/site-recovery/site-recovery-create-recovery-plans) and [run automation scripts as part of failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-runbook-automation)<br>
- [Sample scripts to Automate different operations during failover](https://github.com/Azure/azure-quickstart-templates/tree/master/asr-automation-recovery/scripts)<br>
- [Script to assign public IP address to failed over VM](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-AddPublicIp.ps1)<br>
- [Script to update DNS records of the VM being failed over](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-DNS-UpdateIP.ps1)<br>
