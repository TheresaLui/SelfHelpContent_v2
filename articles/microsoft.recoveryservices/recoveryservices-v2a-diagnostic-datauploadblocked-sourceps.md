<properties
    pageTitle="Your virtual machine is not able to upload data to process server"
    description="Your virtual machine is not able to upload data to process server"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="ramamill"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_DataUploadBlockedFromSourceToPS"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Your virtual machine is not able to upload data to process server
<!--issueDescription-->
Generation of crash and application consistency points has failed because your virtual machine is not able to upload data to process server. This is more frequently seen if virtual machine is not able to reach the process server.
<!--/issueDescription-->

## **Recommended Steps**

- Verify that the process server is up and [healthy](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health)
- Verify that your virtual machine is up and running
- Login to the process server as an administrator and restart the service "cxprocessserver"
- Login to the virtual machine as an administrator and restart the service "InMage Scout VX Agent-Sentinel/Outpost (svagents)"
- In the virtual machine, run "cxpsclient" tool to check the network connectivity. To do that, run `cxpsclient -i <ProcessServer_IP> -l 9443 -v 2`.
- If the issue persists, check the log in "C:\Program Files (X86)\Microsoft Azure Site Recovery\agent\svagents*log" on the virtual machine for detailed information
- On the process server, check the log in "C:\ProgramData\ASR\home\svsystems\transport\log\cxps*log" for detailed error information
- [Troubleshoot VMware-to-Azure VM replication issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication)

## **Recommended Documents**

- Learn more about [monitoring requirements](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-monitor-process-server#monitor-process-server-health) to avoid such issues in the future
