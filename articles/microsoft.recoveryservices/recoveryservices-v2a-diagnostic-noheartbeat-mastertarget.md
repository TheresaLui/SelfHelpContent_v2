<properties
    pageTitle="Master target server is unable to communicate with configuration server"
    description="Master target server is unable to communicate with configuration server"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="ramamill"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_NoHeartbeatFromMasterTarget"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Master target server is unable to communicate with Configuration Server
<!--issueDescription-->
For healthy DR operations, connectivity is necessary between all Site Recovery components. Master target server is unable to communicate with configuration server.
<!--/issueDescription-->

## **Recommended Steps**

- Verify that the master target server is up and running
- Login to master target server as an administrator and restart the Svagents (InMage Scout VX Agent) service
- If the issue persists, check the log at `C:\ProgramData\ASR\agent\svagents*log` for error details

## **Recommended Documents**

- Learn more about [troubleshooting](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication) application or crash consistency point generation failures
- Learn more about [monitoring requirements](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-monitor-process-server#monitor-process-server-health) to avoid such issues in the future
