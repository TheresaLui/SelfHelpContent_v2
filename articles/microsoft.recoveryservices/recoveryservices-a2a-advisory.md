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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a3824214-29ab-41a8-b820-df79ac70d7c7"
	ownershipId="Compute_SiteRecovery"
/>

# Advisory Questions - Azure to Azure

**Note**: Azure to Azure does not support migration of Azure VMs between the same region.

## **Recommended Documents**

- [What are the supported and not supported configurations for Azure to Azure replication?](https://docs.microsoft.com/azure/site-recovery/site-recovery-support-matrix-azure-to-azure)<br>
- [What are the prerequisites for Azure to Azure replication?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-walkthrough-prerequisites)<br>
- [Application and  Crash consistent recovery points details](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#what-is-an-application-consistent-recovery-point)
- [How does the IP assignment happen in Failover and Test Failover](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#after-failover-the-server-doesnt-have-the-same-ip-address-as-the-source-vm-why-is-it-assigned-a-new-ip-address)</br>
- [How do I find the RTO?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#how-can-i-find-the-rto-of-a-recovery-plan)
- [Pricing - What charges do I incur while using Azure Site Recovery?](https://azure.microsoft.com/blog/know-exactly-how-much-it-will-cost-for-enabling-dr-to-your-azure-vm/)</br>
- [ Site Recovery with Azure Backup supported scenarios](https://docs.microsoft.com/azure/site-recovery/site-recovery-backup-interoperability)

### **Networking**

* [How to retain private ip address in DR region](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#can-i-retain-a-private-ip-address-during-failover)</br>
* [Can I retail Public IP ?](https://docs.microsoft.com/azure/site-recovery/concepts-public-ip-address-with-site-recovery#public-ip-address-assignment-using-recovery-plan)</br>
* [Using NSG with Site Recovery](https://docs.microsoft.com/azure/site-recovery/concepts-network-security-group-with-site-recovery#using-network-security-groups)</br>

### **Replication**

* [How to enable consistent recovery points across multiple servers](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#multi-vm-consistency)</br>
* [How replication points are generated](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#replication-policy)</br>
* [How to automate disaster recovery of Azure virtual machines using PowerShell](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-powershell)</br>
* [What all does Azure Site Recovery replicates to target region](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture#target-resources)</br>

### **Failover**

* [What happen in case my primary Azure region has an outage?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#if-im-replicating-between-two-azure-regions-what-happens-if-my-primary-region-experiences-an-unexpected-outage)</br>
* [Is failover automatic?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#is-failover-automatic)

### **Reprotect and Failback**

* [How much time does it take to fail back?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#reprotection-and-failback)

### **Replicate IaaS VMs from one Azure region to another Azure region**

* [Review the architecture for Azure VM replication between Azure regions](https://docs.microsoft.com/azure/site-recovery/concepts-azure-to-azure-architecture)<br>
* [Troubleshoot Azure to Azure VM replication issues](https://docs.microsoft.com/azure/site-recovery/site-recovery-azure-to-azure-troubleshoot-errors)
* [**Refer to the most frequently asked questions before filing a support case**](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-common-questions)
