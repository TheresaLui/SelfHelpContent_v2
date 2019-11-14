<properties
    pageTitle="Your virtual machine is not able to reach process server"
    description="Your virtual machine is not able to reach process server"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="ramamill"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_ProcessServerNotReachableFromSourceVm"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Your virtual machine is not able to reach process server
<!--issueDescription-->
Mobility agent installed on the server is not able to communicate with process server. Therefore, generation of crash and application consistency points is impacted.
<!--/issueDescription-->

## **Recommended Steps**

- Verify that the process server is up and [healthy](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health)
- Verify that your virtual machine is up and running
- Login to the process server as an administrator and restart the service "cxprocessserver"
- Login to the virtual machine as an administrator or root user and run "cxpsclient" tool to check the network connectivity. To do that, run `cxpsclient -i <ProcessServer_IP> -l 9443 -v 2`.
- If the issue persists, check the log in "C:\ProgramData\ASR\home\svsystems\transport\log\cxps*log" on the process server for detailed error information

## **Recommended Documents**

- [Troubleshoot VMware-to-Azure VM replication issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication)
