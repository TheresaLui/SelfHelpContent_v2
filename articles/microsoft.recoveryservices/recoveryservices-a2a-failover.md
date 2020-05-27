<properties
	pageTitle="Failover A2A"
	description="Failover A2A"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="v-bllydi"
    ms.author="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32574719"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="088066b0-5fd9-476a-9fa2-6d6949c584ef"
	ownershipId="Compute_SiteRecovery"
/>

# Failover and Failback Azure VM between Azure regions

## **Recommended Documents**

- [How to fail over and fail back Azure VMs between Azure regions](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failover-failback)<br>
- [How to retain fixed IP address after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-retain-ip-azure-vm-failover)<br>
- [How to retain Public IP address to a VM after failover](https://docs.microsoft.com/azure/site-recovery/concepts-public-ip-address-with-site-recovery#public-ip-address-assignment-using-recovery-plan)<br>
- [Is Failover automatic?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#is-failover-automatic)
- [How is capacity assured in DR region for Azure VMs?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#how-is-capacity-assured-in-target-region-for-azure-vms-1)
- [How much time does it take to fail back?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#how-much-time-does-it-take-to-fail-back)
- [How to replicate NSG with ASR](https://docs.microsoft.com/azure/site-recovery/concepts-network-security-group-with-site-recovery#azure-to-azure-replication-with-nsg)
- [Why virtual machines are not cleaned up after failback](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failback#fail-back-to-the-primary-region)
- [How to troubleshoot RDP connection to Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)<br>
- [How to troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)<br>

**Troubleshooting**

- There aren't sufficient cores available to failover? Follow [these steps](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request) to increase the quota.
- Troubleshooting Failover error codes with: [Error ID 28031](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28031), [Error ID 28092](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28092), [Error ID 70038](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-70038)<br>