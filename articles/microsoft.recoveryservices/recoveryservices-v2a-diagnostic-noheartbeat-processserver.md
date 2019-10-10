<properties
    pageTitle="Process Server is unable to communicate with Configuration Server"
    description="Process Server is unable to communicate with Configuration Server"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="ramamill"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_NoHeartbeatFromProcessServer"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Process Server is unable to communicate with Configuration Server
<!--issueDescription-->
Azure Site Recovery service "tmansvc" on Process Server is unable to communicate with Configuration Server. For healthy DR operations, connectivity is necessary between all Site Recovery components.
<!--/issueDescription-->

## **Recommended Steps**

- Verify that the master target server is up and running
- Login to Process Server as an administrator and restart the tmansvc service
- Verify that the Process Server is [healthy](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health)
- If issue persists, check following logs on the Process Server for error details:

  - C:\ProgramData\ASR\home\svsystems\eventmanager*log
  - C:\ProgramData\ASR\home\svsystems\monitor_protection*.log

## **Recommended Documents**

- Learn more about [troubleshooting](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication) application or crash consistency point generation failures
- Learn more about [monitoring requirements](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-monitor-process-server#monitor-process-server-health) to avoid such issues in the future
