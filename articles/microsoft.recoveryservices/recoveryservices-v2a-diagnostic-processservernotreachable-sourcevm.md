<properties
    pageTitle="Replication is not progressing as Process Server is not reachable"
    description="Replication status is critical because ASR agent on Source Machine is not able to connect to Process Server."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_ProcessServerNotReachableFromSourceVm"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Replication is not progressing as Process Server is not reachable

<!--issueDescription-->
Replication status is critical because Azure Site Recovery agent on Source Machine is not able to connect to Process Server.
<!--/issueDescription-->

## **Recommended Steps**

Verify the network connectivity from source VM to Process Server. To do that, follow these steps:

1. Verify the Process Server machine is up and running
2. Login to Process Server with administrator privileges
3. Verify that the service **cxprocessserver** is running, then start or restart the service
4. Login to source VM with administrator (root user on Linux OS) privileges
5. Run **cxpsclient** tool to check network connectivity: cxpsclient -i <Process_Server_IP> -l 9443 -v 2
6. On the Process Server, check the following log for any errors "C:\\ProgramData\\ASR\\home\\svsystems\\transport\\log\\cxps*log"

## **Recommended Documents**

- [Troubleshoot VMware-to-Azure VM replication issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication)
