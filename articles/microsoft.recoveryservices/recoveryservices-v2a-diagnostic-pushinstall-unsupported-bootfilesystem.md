<properties
    pageTitle="Push installation failed because unsupported boot file system found"
    description="Push installation of mobility agent fails because root account is not provided in linux VMs"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_UnsupportedBootFileSystem"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push Installation of Mobility agent fails because of unsupported boot file system

<!--issueDescription-->
Push installation fails because the source machine has unsupported boot file system. Before version 9.20 about Azure Site Recovery(ASR) components, configuration of boot on a Logical Volume Manager device is not unsupported.
<!--/issueDescription-->

## **Recommended Steps**

Upgrade ASR components to the latest version for this support.
