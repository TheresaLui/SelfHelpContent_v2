<properties
	pageTitle="E2A replication does not progress"
	description="E2A  replication does not progress"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536440"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
	articleId="24c58cd6-d0e3-4665-8ea3-89757767e4c5"
/>
# Is replication not progressing when replicating VMs on Hyper-V hosts managed by SCMM?

## **Recommended Steps**

Verify that your configuration is supported by Azure Site Recovery. For information about supported configurations, see the [Supported/Not-supported configurations matrix](https://docs.microsoft.com/azure/site-recovery/support-matrix-hyper-v-to-azure) for Hyper-V to Azure replication.<br>

Follow the Deployment planner recommendations for a successful disaster recovery in [About the Azure Site Recovery Deployment Planner for Hyper-V disaster recovery to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-hyper-v-deployment-planner)?<br>

## **Recommended documents**

- [Enable protection failed? Cannot Enable replication?](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#enable-protection-issues)<br>
- [Replication not progressing? Replication stuck?](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#replication-issues)<br>
- [The virtual machine couldn't be replicated?](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#replication-issues)<br>
- [VM Replication health is in critical state?](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#replication-issues)<br>
- [Not seeing App-Consistent recovery points?](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#app-consistent-snapshot-issues)<br>
- [ErrorCode: 0x800700EA Error Message: Hyper-V failed to generate VSS snapshot set for virtual machine](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#common-errors)
- [ErrorCode: 0x80070032 Error Message: Hyper-V Volume Shadow Copy Requestor failed to connect to virtual machine](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#common-errors)
- [Replication errors occurred for VM because of issues with connectivity to Azure storage](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#replication-issue)<br>
