<properties
    pageTitle="Your process server is not able to reach Azure"
    description="Your process server is not able to reach Azure"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="ramamill"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_ReplicationBlockedCritical"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Your process server is not able to reach Azure
<!--issueDescription-->
Process server is not able to transfer data to Azure. Therefore, generation of crash and application consistency points is impacted.
<!--/issueDescription-->

## **Recommended Steps**

- Verify that the process server is up and [healthy](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health)
- Verify that your virtual machine is up and running
- Login to the process server as an administrator and restart the service "cxprocessserver"
- Login to the virtual machine as an administrator or root user and run "cxpsclient" tool to check the network connectivity. To do that, run `cxpsclient -i <ProcessServer_IP> -l 9443 -v 2`.
- If the issue persists, check the log in "C:\ProgramData\ASR\home\svsystems\transport\log\cxps*log" on the process server for detailed error information

## **Recommended Documents**

- Learn more about [troubleshooting](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication) application or crash consistency point generation failures
- Learn more about [monitoring requirements](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-monitor-process-server#monitor-process-server-health) to avoid such issues in the future
