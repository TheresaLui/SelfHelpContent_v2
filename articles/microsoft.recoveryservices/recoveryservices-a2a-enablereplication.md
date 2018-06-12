<properties
	pageTitle="A2A enable replication"
	description="A2A enable replication"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="v-bllydi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32574718"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
/>
# Replicate Azure VMs from one Azure region to another Azure region using Azure Site Recovery

## **Recommended steps**

* **Unsupported Scenarios**</br>
	-  Cross subscription migration and ASM to ARM, [here](https://docs.microsoft.com/azure/site-recovery/site-recovery-migrate-azure-to-azure) are the workarounds.</br>
	- Migration of IAAS VMs between the same region.</br>
	- Workloads in Azure to Azure scenario must be migrated as an entire VM</br>
- Review the [**Support Requirements**](https://docs.microsoft.com/azure/site-recovery/site-recovery-support-matrix-azure-to-azure) for all components.</br>
- [Troubleshooting common Azure to Azure VM replication issues](https://docs.microsoft.com/azure/site-recovery/site-recovery-azure-to-azure-troubleshoot-errors)</br>
- [What charges do I incur while using Azure Site Recovery?](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#pricing)</br>

## **Recommended documents** 

- Understand the [scenario architecture and components](https://docs.microsoft.com/azure/site-recovery/concepts-azure-to-azure-architecture)</br>
- [Steps to **enable replication** for Azure VMs](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-walkthrough-enable-replication)</br>
- [**Networking guidance** for replicating Azure virtual machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-walkthrough-network)</br>
- [Steps to configuring outbound network connectivity](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication#configure-outbound-network-connectivity)
