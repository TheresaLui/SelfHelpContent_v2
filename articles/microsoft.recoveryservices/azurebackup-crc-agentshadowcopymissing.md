    
<properties
    pageTitle="AgentShadowCopyMissing"
    description="AgentShadowCopyMissing"
    infoBubbleText="Backup failed because of insufficient shadow copy space in the selected backup volume(s)."
    service="microsoft.recoveryservices"
    resource="backup"
    authors="srinathvasireddy"
    ms.author="srinathvasireddy"
    displayOrder=""
    articleId="azurebackup-crc-agentshadowcopymissing"
    diagnosticScenario="azurebackup-crc-agentshadowcopymissing"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>


# Error AgentShadowCopyMissing

<!--issueDescription-->
We have identified that your backup operation failed because of insufficient shadow copy space in the selected backup volume(s).
<!--/issueDescription-->


## **Recommended Steps**

To resolve this issue, perform the below:

- Increase Shadow copy storage space for the affected volume(s) using the vssadmin tool, restart the VSS service and try again
- To resolve snapshot deleted due to high IO on the volume, try scheduling backup when there is low IOPS load (for ex. off-peak hours) on the source volumes
