<properties
    pageTitle="The Site recovery process Server is not uploaded from last 60 minutes"
    description="Replication status is critical because the replication data on Process Server is not uploaded from last 60 minutes."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="genlin"
    ms.author="asgang,genli"
    displayOrder=""
    articleId="ASR_ReplicationNotProgressing_DiskSessionNotProcessing"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Replication status is critical because the Process Server is not uploaded from last 60 minutes
<!--issueDescription-->
We detect that the replication status is critical because replication data on Process Server is not uploaded from last 60 minutes.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the problem, follow these steps:

1. Check MARS agent logs for any upload errors.
2. Check the ASR service svagents is running. If not start/restart the service
3. Check the network connectivity to the Azure storage from the Process Server.
