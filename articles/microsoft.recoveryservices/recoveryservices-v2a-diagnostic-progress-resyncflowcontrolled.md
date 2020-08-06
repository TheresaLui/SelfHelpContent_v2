<properties
    pageTitle="Azure Recovery Services agent failed to upload replication data"
    description="Initial replication of VM is stuck as MARS is failing to upload replication data to Azure"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="genlin"
    ms.author="asgang,genli"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_ReSyncFlowControlled"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Replication status is critical because Azure Recovery Services failed to upload replication data
<!--issueDescription-->
We detect that the replication is not progressing because **Microsoft Azure Recovery Services Agent** service failed to upload replication data.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the problem,  make sure that the **Microsoft Azure Recovery Services Agent** service is not blocked by antivirus program or firewall in the virtual machine.
