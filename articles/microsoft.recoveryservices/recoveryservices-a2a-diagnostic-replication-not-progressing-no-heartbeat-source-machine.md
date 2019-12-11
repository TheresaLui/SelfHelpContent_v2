<properties
    pageTitle="Replication is not progressing with no heartbeat from Source Machine"
    description="Replication status is critical because of the ASR agent on Source Machine is not able to connect to Site Recovery Server endpoints."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_NoHeartbeatFromSourceMachine"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Replication is not progressing with no heartbeat from Source Machine

<!--issueDescription-->
Replication status is critical because the Azure Site Recovery agent on Source Machine is not able to connect to Site Recovery Server endpoints.
<!--/issueDescription-->

## **Recommended Steps**

Verify the heartbeat for Source Machine. To do that, follow these steps:

1. Verify the Source Machine is up and running.
2. Login to Source Machine with administrator privileges on Windows OS or as user root on Linux OS.
3. Verify that the service **Svagents (InMage Scout VX Agent)** is running. And then, start or restart the service.
4. On the Source Machine, check the following log for any errors:

    - **Windows**: C:\\Program Files (x86)\\Microsoft Azure Site Recovery\\agent\\svagents*log.  
    - **Linux**: /var/log/svagents*log.
