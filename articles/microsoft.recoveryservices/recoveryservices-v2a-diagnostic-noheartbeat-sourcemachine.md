<properties
    pageTitle="Virtual machine is unable to communicate with configuration server"
    description="Virtual machine is unable to communicate with configuration server"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="ramamill"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_NoHeartbeatFromSourceMachine"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Your virtual machine is unable to communicate with Configuration Server
<!--issueDescription-->
Mobility agent on your virtual machine is unable to communicate with Configuration Server. For healthy DR operations, connectivity is necessary between all Site Recovery components.
<!--/issueDescription-->

## **Recommended Steps**

- Verify that your virtual machine is is up and running
- Login to the machine as an administrator and restart the services:

  - Svagents (InMage Scout VX Agent)
  - InMage Scout Application Service
  
- If the issue persists, check the log at "C:\Program Files (X86)\Microsoft Azure Site Recovery\agent\svagents*log" for error details

## **Recommended Documents**

- Learn more about [troubleshooting](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication) application or crash consistency point generation failures
