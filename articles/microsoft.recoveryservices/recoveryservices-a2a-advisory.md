<properties
	pageTitle="Site Recovery (Azure to Azure)/Enable Replication"
	description="Site Recovery (Azure to Azure)/Common issues during Enable Replication"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32574716"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Can't Enable Replication? Initial Replication Failing?

## **Recommended documents**

- [What are the supported and not supported configurations for Azure to  Azure replicaton?](https://docs.microsoft.com/azure/site-recovery/site-recovery-support-matrix-azure-to-azure)<br>
- [What are the pre-requisites for Azure to Azure replication?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-walkthrough-prerequisites)<br>
- At present Azure to Azure **does not support cross subscription migration and ASM to ARM**, as a workaround follow the steps mentioned [here](https://docs.microsoft.com/azure/site-recovery/site-recovery-migrate-azure-to-azure).<br>
- Azure to Azure **does not support migration of IAAS VMs between the same region**.<br>
- [How to troubleshoot Azure to Azure VM replication issues?](https://docs.microsoft.com/azure/site-recovery/site-recovery-azure-to-azure-troubleshoot-errors)<br>
- [What charges do I incur while using Azure Site Recovery?](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#pricing)<br>

**How to Replicate IaaS VMs from one Azure region to another Azure region?**<br>
- [Review the architecture for Azure VM replication between Azure regions](https://docs.microsoft.com/azure/site-recovery/concepts-azure-to-azure-architecture)<br>
- [**Networking guidance** for replicating Azure virtual machines](https://docs.microsoft.com/azure/site-recovery/site-recovery-azure-to-azure-networking-guidance)<br>
- [How to **enable replication** for Azure VMs?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication)<br>
- [How to run a **test failover** for Azure VM replication?](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-dr-drill)<br>
- [How to **re-protect (Failback)** from failed over Azure region back to primary region?](https://docs.microsoft.com/azure/site-recovery/site-recovery-how-to-reprotect-azure-to-azure)<br>
