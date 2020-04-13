<properties
    pageTitle="Enable protection fails because of special characters on source mobility drive"
    description="Enable protection fails because of special characters on source mobility drive"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_CSRefreshFabricFailure_SpecialChar"
    diagnosticScenario="ASRV2ACSInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable protection fails because of special characters on source mobility drive

<!--issueDescription-->
Communication to the configuration server fails with error **InMageGetPriVmPlacementPropDraError**. This is caused by the special characters on the source mobility drive.
<!--/issueDescription-->

## **Recommended Steps**

Remove the special characters from the volume label on the Windows operating system and retry the Enable Protection job.
