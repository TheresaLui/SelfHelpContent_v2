<properties
    pageTitle="Mobility agent installation fails due to VSS provider installation failure"
    description="Mobility agent installation fails due to VSS provider installation failure"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_MobilityAgentInstallFailure_VSSProviderInstallationFailed"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Mobility agent installation fails due to VSS provider installation failure

<!--issueDescription-->
VSS installation is a part of Mobility agent installation. This service is used in the process of generating application consistent recovery points. This step fails due to some internal errors, leading to push installation failure.
<!--/issueDescription-->

## **Recommended Steps**

Identify the exact errors under C:\ProgramData\ASRSetupLogs\ASRUnifiedAgentInstaller.log. Few common errors and resolution steps are listed [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#lvm-support-from-920-version).
