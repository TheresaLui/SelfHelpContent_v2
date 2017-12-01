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
	productPesIds="15207"
	cloudEnvironments="public"
/>
# Replicate Azure VMs from one Azure region to another Azure region using Azure Site Recovery

## **Recommended steps**
- **Unsupported Scenarios**</br>
	-  Cross subscription migration and ASM to ARM, [here](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-migrate-azure-to-azure) are the workarounds.
	- Migration of IAAS VMs between the same region.
	- Workloads in Azure to Azure scenario must be migrated as an entire VM
- Review the [**Support Requirements**](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-azure-to-azure) for all components.
- [Troubleshooting common Azure to Azure VM replication issues](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-azure-to-azure-troubleshoot-errors)
- [What charges do I incur while using Azure Site Recovery?](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-faq#pricing)

## **Recommended documents**
- Understand the [scenario architecture and components](https://docs.microsoft.com/en-us/azure/site-recovery/concepts-azure-to-azure-architecture).
- [Steps to **enable replication** for Azure VMs](https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-walkthrough-enable-replication)
- [**Networking guidance** for replicating Azure virtual machines](https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-walkthrough-network)
- [Steps to configuring outbound network connectivity](https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-tutorial-enable-replication#configure-outbound-network-connectivity)
