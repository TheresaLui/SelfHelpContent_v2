<properties
    pageTitle="Replication is not progressing as disk is removed on Source Machine"
    description="Replication status is critical because a replicating disk on Source Machine is removed."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_DiskRemoved"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Replication is not progressing as disk is removed

<!--issueDescription-->
Replication status is critical because a replicating disk on the Source Machine is removed.
<!--/issueDescription-->

## **Recommended Steps**

Verify the disks on Source Machine. To do that, follow these steps:

1. Login to Source Machine with administrator privileges on Windows or as user root on Linux.
2. Verify the number of disks and their signatures are matching with the data in telemetry.
3. If disk remove is confirmed, disable and enable replication.
4. On the Source Machine, check the following log for any errors:

    - **Windows**: C:\\Program Files (x86)\\Microsoft Azure Site Recovery\\agent\\svagents*log.  
    - **Linux**: /var/log/svagents*log.
