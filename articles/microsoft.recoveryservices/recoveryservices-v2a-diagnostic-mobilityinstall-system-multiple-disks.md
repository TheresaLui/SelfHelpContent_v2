<properties
    pageTitle="Root file system is laid on multiple disks"
    description="Root file system is laid on multiple disks"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_MobilityAgentInstallFailure_SystemPartitionOnMultipleDisks"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Root file system is laid on multiple disks

<!--issueDescription-->
The root file system is laid on multiple disks (Logical Volume Manager configuration), which is an unsupported scenario.
<!--/issueDescription-->

## **Recommended Steps**

Accommodate both root and boot file systems to a single disk and then enable the protection.
