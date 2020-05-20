<properties
    pageTitle="Boot and system partition are not on same disk"
    description="Boot and system partition are not on same disk"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_MobilityAgentInstallFailure_BootAndSystemPartitionNotOnSameDisk"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Boot and system partition are not on same disk

<!--issueDescription-->
Either root file system is laid on multiple disks (Logical Volume Manager configuration) or root and boot file systems laid on completely different disks, which is an unsupported scenario.
<!--/issueDescription-->

## **Recommended Steps**

Accommodate both root and boot file systems in the same disk and then enable the protection.
