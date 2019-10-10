<properties
    pageTitle="Date churn rate on source virtual machine exceeded supported limits"
    description="Date churn rate on source virtual machine exceeded supported limits"
    infoBubbleText="The disk data change rate on the source virtual machine exceeded supported limits."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang"
    ms.author="asgang,genli"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_SourceMachineChurnRateExceeded"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Date churn rate on source virtual machine exceeded supported limits
<!--issueDescription-->
The Replication status is critical because the disk data change rate on the source virtual machine exceeded supported limits. Azure Site Recovery has limits on data change rate, based on the type of disk.
<!--/issueDescription-->

## **Recommended Steps**

1. Check [Azure Site Recovery Limit](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#azure-site-recovery-limits).
2. [Identify the disk that](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#solution) is churning at higher than supported rate.
3. Exclude the disk that causes a high data-change rate, or upgrade the disk to higher tier if it is possible.

If you cannot remove the disk or the higher tier disk still cannot resolve the issue, the site recovery service may not apply to the source virtual machine.

## **Recommended Documents**

* [High data change rate on the source virtual machine](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#high-data-change-rate-on-the-source-virtal-machine)
