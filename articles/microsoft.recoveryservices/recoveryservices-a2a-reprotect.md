<properties
	pageTitle="Reprotect-A2A"
	description="Reprotect- A2A"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="v-bllydi"
    ms.author="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32574723"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a7ee66ca-fb61-41f7-a8a4-6b2afcd87232"
	ownershipId="Compute_SiteRecovery"
/>

# Reprotecting the Azure VM in the secondary region

## **Recommended Steps**

- [What happens during re-protection?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-how-to-reprotect#what-happens-during-reprotection)
- [Powershell command to re-protect](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-powershell#reprotect-and-failback-to-source-region)
- [Does Site Recovery replicates complete data during re-protection?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#at-the-time-of-reprotection-does-site-recovery-replicate-complete-data-from-the-secondary-region-to-the-primary-region)
- [How much time does it take to fail back?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#how-much-time-does-it-take-to-fail-back)
- [Why virtual machines are not cleaned up after fail back?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failback#fail-back-to-the-primary-region)
- [Re-protection failure](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#issue-1-failed-to-register-azure-virtual-machine-with-site-recovery-151195-br) due to DNS connectivity issue.
- After VMs are [re-protected](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failover-failback#reprotect-the-secondary-vm), to go back (fail back) to the primary region follow these [fail over](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failover-failback) instructions.<br>

## **Recommended Documents**

- [How to fail over and re-protect Azure VMs between Azure regions](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failover-failback)</br>
- [How to fail back after Failover](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failback)
- [How to connect to a VM after fail over to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)
