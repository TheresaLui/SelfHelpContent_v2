<properties
    pageTitle="Communication to configuration server fails because FIPS compliance is enabled"
    description="Communication to configuration server fails because FIPS compliance is enabled"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_CSInstallFailure_FIPSEnabled"
    diagnosticScenario="ASRV2ACSInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Communication to configuration server fails because FIPS compliance is enabled

<!--issueDescription-->
Communication to the configuration server fails with error **InMageGetPriVmPlacementPropDraError** because the FIPS compliance is enabled.
<!--/issueDescription-->

## **Recommended Steps**

1. On the configuration server, go to HKEY_LOCAL_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Lsa\\ registry hives and set the value of **fipsalgorithmpolicy** to 0.
2. Reboot the configuration server and then retry the operation.
