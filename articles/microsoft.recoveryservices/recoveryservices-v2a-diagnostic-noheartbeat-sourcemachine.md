<properties
    pageTitle="Replication is not progressing with no heartbeat from Source Machine"
    description="Replication status is critical because ASR agent on Source Machine is not able to connect to Configuration Server."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_NoHeartbeatFromSourceMachine"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Replication is not progressing with no heartbeat from Source Machine

<!--issueDescription-->
Replication status is critical because Azure Site Recovery agent on Source Machine is not able to connect to Configuration Server.
<!--/issueDescription-->

## **Recommended Steps**

Verify the heartbeat for Source Machine. To do that, follow these steps:

1. Verify the Source Machine is up and running
2. Login to Source Machine with administrator privileges
3. Verify that the service **svagents** and **InMage Scout Application Service** are running and then start or restart the services
4. On the Source Machine, check the following log for any errors in C:\\Program Files (x86)\\Microsoft Azure Site Recovery\\agent\\svagents*log
