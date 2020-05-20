<properties
    pageTitle="Replication is not progressing as data tracking module is not Loaded"
    description="Replication status is critical because on Source Machine the ASR agent's data tracking module is not loaded."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_DataTrackingModuleNotLoaded"
    diagnosticScenario="ASRA2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Replication is not progressing as data tracking module is not Loaded

<!--issueDescription-->
Replication status is critical because the Azure Site Recovery(ASR) agent's data tracking module on Source Machine is not loaded.
<!--/issueDescription-->

## **Recommended Steps**

Verify the data tracking module status. To do that, follow these steps:

1. Login to Source Machine as user root
2. Verify the Linux kernel version (ex: # uname -r) is supported by the currently installed ASR Mobility Service version
3. Upgrade to the latest Mobility Service version that [supports for the kernel](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#replicated-machine-operating-systems) if required
4. On the Source Machine, check the following log for any errors in "/var/log/svagents*log"
