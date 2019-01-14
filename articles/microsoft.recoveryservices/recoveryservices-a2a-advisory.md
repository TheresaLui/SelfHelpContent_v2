<properties
	pageTitle="Site Recovery (Azure to Azure)/Enable Replication"
	description="Site Recovery (Azure to Azure)/Advisory questions - Azure to Azure"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630515"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
/>

# Advisory Questions - Azure to Azure

**Note**: Azure to Azure **does not support migration of IAAS VMs between the same region**.

## **Recommended Documents**

- [What are the supported and not supported configurations for Azure to  Azure replicaton?](https://docs.microsoft.com/azure/site-recovery/site-recovery-support-matrix-azure-to-azure)<br>
- [What are the pre-requisites for Azure to Azure replication?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-walkthrough-prerequisites)<br>
- [ How can I find the RTO.](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#how-can-i-find-the-rto-of-a-recovery-plan)
- [What charges do I incur while using Azure Site Recovery?](https://azure.microsoft.com/blog/know-exactly-how-much-it-will-cost-for-enabling-dr-to-your-azure-vm/)</br>
- Frequenctly asked questions on [Replication,](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#replication)[ Replication Policy,](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#replication-policy)[ Multi-VM Consistency,](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#multi-vm-consistency)[ Failover,](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#failover)[ Recovery Plan,](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#recovery-plan)[ Reprotect & Failback.](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#reprotection-and-failback) </br>

**Replication**</br>
[How to enable consistent recovery points across multiple servers.](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#multi-vm-consistency)</br>
[How replication points are generated.](https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-common-questions#replication-policy)</br>
[How to automate disaster recovery of Azure virtual machines using PowerShell.](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-powershell)</br>
[ What all does ASR replicates to target region.](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture#target-resources)</br>

**Networking**</br>
[How to retain private ip address in DR region.](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#can-i-retain-a-private-ip-address-during-failover)</br>
[How to use Public IP with Site Recovery.](https://docs.microsoft.com/azure/site-recovery/concepts-public-ip-address-with-site-recovery)</br>
[Using NSG with Site Recovery.](https://docs.microsoft.com/azure/site-recovery/concepts-network-security-group-with-site-recovery#using-network-security-groups)</br>

**Failover**</br>
[How does the IP assignment happen in Failover and Test Failover.](https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-common-questions#after-failover-the-server-doesnt-have-the-same-ip-address-as-the-source-vm-why-is-it-assigned-a-new-ip-address)</br>
[What happen in case my primary Azure region has an outage.](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#if-im-replicating-between-two-azure-regions-what-happens-if-my-primary-region-experiences-an-unexpected-outage)</br>
[Is failover automatic?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#is-failover-automatic)

**Reprotect and Failback**</br>
[How much time does it take to fail back?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#reprotection-and-failback)

**Replicate IaaS VMs from one Azure region to another Azure region**<br>
- [Review the architecture for Azure VM replication between Azure regions.](https://docs.microsoft.com/azure/site-recovery/concepts-azure-to-azure-architecture)<br>
- [Troubleshoot Azure to Azure VM replication issues.](https://docs.microsoft.com/azure/site-recovery/site-recovery-azure-to-azure-troubleshoot-errors)<br>
