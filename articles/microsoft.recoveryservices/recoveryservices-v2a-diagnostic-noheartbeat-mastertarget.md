<properties
    pageTitle="Replication is not progressing with no heartbeat from Master Target"
    description="Replication status is critical because ASR agent on Master Target is not able to connect to Configuration Server."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_NoHeartbeatFromMasterTarget"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Replication is not progressing with no heartbeat from Master Target

<!--issueDescription-->
Replication status is critical because agent on Master Target is not able to connect to Configuration Server.
<!--/issueDescription-->

## **Recommended Steps**

Verify the heartbeat from Master Target. To do that, follow these steps:

1. Verify the Master Target machine is up and running
2. Login to Master Target with administrator privileges
3. Verify that the service **svagents** is running, then start or restart the service
4. On the Master Target, check the following log for any errors in "C:\\ProgramData\\ASR\\agent\\svagents*log"
