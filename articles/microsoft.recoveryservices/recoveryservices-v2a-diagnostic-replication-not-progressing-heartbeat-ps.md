<properties
    pageTitle="Replication is not progressing with no heartbeat from Process Server"
    description="Replication status is critical because the ASR service on Process Server is not able to connect to Configuration Server."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_NoHeartbeatFromProcessServer"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Replication is not progressing with no heartbeat from Process Server

<!--issueDescription-->
Replication status is critical because the Azure Site Recovery service on Process Server is not able to connect to Configuration Server.
<!--/issueDescription-->

## **Recommended Steps**

Verify the heartbeat from Process Server. To do that, follow these steps:

1. Verify the Process Server machine is up and running.
2. Login to Process Server with administrator privileges.
3. Verify that the service **tmansvc** is running. And then, start or restart the service.
4. On the Process Server, check the following logs for any errors:

    - C:\\ProgramData\\ASR\\home\\svsystems\\eventmanager*log.
    - C:\\ProgramData\\ASR\\home\\svsystems\\monitor_protection*.log.
