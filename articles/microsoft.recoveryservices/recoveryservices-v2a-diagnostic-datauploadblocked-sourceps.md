<properties
    pageTitle="Replication is not progressing with data upload blocked from Source to Process Server"
    description="Replication status is critical because replication data from ASR agent on Source Machine is not uploaded to Process Server."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_ReplicationNotProgressing_DataUploadBlockedFromSourceToPS"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Replication is not progressing with data upload blocked from Source to Process Server

<!--issueDescription-->
Replication status is critical because replication data from Azure Site Recovery(ASR) agent on Source Machine is not uploaded to Process Server.
<!--/issueDescription-->

## **Recommended Steps**

Verify the ASR agent running status and network connectivity from source VM to Process Server. To do that, follow these steps:

1. Verify the Process Server machine is up and running
2. Login to Source Machine and Process Server with administrator privileges
3. Verify that the service **cxprocessserver** is running on Process Server, then start or restart the service
4. Login to source VM with administrator (root user on Linux OS) privileges
5. Verify that the service **svagents (InMage Scout VX Agent)** is running and start or restart it if required
6. Run **cxpsclient** tool to check network connectivity: cxpsclient -i <Process_Server_IP> -l 9443 -v 2
7. On the Source Machine, check the following log for any errors: C:\\Program Files (x86)\\Microsoft Azure Site Recovery\\agent\\svagents*log
8. On the Process Server, check the following log for any errors: "C:\\ProgramData\\ASR\\home\\svsystems\\transport\\log\\cxps*log"
