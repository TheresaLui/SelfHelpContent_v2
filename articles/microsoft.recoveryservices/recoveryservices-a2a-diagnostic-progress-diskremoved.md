<properties
    pageTitle="A replicating disk on the source virtual machine cannot be found"
    description="Microsoft Azure has information regarding your issue"
    infoBubbleText="Microsoft Azure has information regarding your issue."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang"
    ms.author="asgang,genli"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_DiskRemoved"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Replication status is critical because a replicating disk on the source virtual machine is removed
<!--issueDescription-->
We detected that a replicating disk on the source virtual machine is removed.
<!--/issueDescription-->

## **Recommended Steps**

If you remove a replicating disk from the resource virtual machine, the replication will stop working. You must disable and enable replication to resolve the issue.