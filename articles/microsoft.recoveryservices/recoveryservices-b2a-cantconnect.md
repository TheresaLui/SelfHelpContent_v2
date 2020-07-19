<properties
	pageTitle="Site Recovery (Hyper-V Site to Azure)/Not able to conect to VM after failover"
	description="Site Recovery (Hyper-V Site to Azure)/Not able to conect to VM after failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="prateek9us"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536423"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="6262174c-b147-4df1-9e30-94ba7693c0b4"
	ownershipId="Compute_SiteRecovery"
/>

# Unable to connect to VM after failover - Hyper-V to Azure
## **Recommended steps**

- [How to **connect to VM** after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)<br>
- [Issue] [*Connect button grayed out on VM*](https://aka.ms/unabletordpssh)<br>
- [Issue] [*Connect button available and unable to RDP/SSH to VM*](https://aka.ms/unabletordpssh)<br>
- [How to] [troubleshoot RDP connection to Windows VM?](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)<br>
- [How to] [troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)<br>


## **Recommended Documents**

**Automation** <br>
- How to customize recovery plan to run automation scripts as part of failover? [Add Azure Automation runbooks to recovery plans ](https://docs.microsoft.com/azure/site-recovery/site-recovery-runbook-automation)<br>
- [Sample scripts to Automate different operations during failover](https://github.com/Azure/azure-quickstart-templates/tree/master/asr-automation-recovery/scripts)<br>
- [Script to assign public IP address to failed over VM](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-AddPublicIp.ps1)<br>
- [Script to update DNS records of the VM being failed over](https://github.com/Azure/azure-quickstart-templates/blob/master/asr-automation-recovery/scripts/ASR-DNS-UpdateIP.ps1)<br>

**IP address**<br>
- [How to retain the fixed IP address while failing over to Azure](https://docs.microsoft.com/azure/site-recovery/concepts-on-premises-to-azure-networking#retaining-ip-addresses)<br>
- [How to assign New IP address to a VM after failover](https://azure.microsoft.com/blog/networking-infrastructure-setup-for-microsoft-azure-as-a-disaster-recovery-site/)<br>
