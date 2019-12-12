<properties
    pageTitle="The Site recovery process Server is not uploaded from last 60 min"
    description="Replication status is critical because the replication data on Process Server is not uploaded from last 60 min."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="genlin"
    ms.author="asgang,genli"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_ReplicationBlockedCritical "
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Replication status is critical because a replicating disk on the source virtual machine is removed
<!--issueDescription-->
We detected that a replicating disk on the source virtual machine is removed. This causes the replication stops working.
<!--/issueDescription-->

## **Recommended Steps**

Verify the disks on Source Machine. To do that, follow these steps:

1. Login to Source Machine with administrator privileges on Windows or as user root on Linux
2. Verify the number of disks and their signatures are matching with the data in telemetry
3. If disk remove is confirmed, disable and enable replication
4. On the Source Machine, check the following log for any errors:

    - **Windows**: C:\\Program Files (x86)\\Microsoft Azure Site Recovery\\agent\\svagents*log
    - **Linux**: /var/log/svagents*log
