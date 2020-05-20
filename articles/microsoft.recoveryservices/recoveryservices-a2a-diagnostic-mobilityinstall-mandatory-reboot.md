<properties
    pageTitle="Reboot is mandatory after Mobility Agent uninstallation"
    description="Reboot is mandatory after Mobility Agent uninstallation"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_MobilityAgentInstallFailure_MandatoryRebootFailure"
    diagnosticScenario="ASRA2AMobilityAgentInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable replication fails because VM is not rebooted

<!--issueDescription-->
Installation of mobility agent failed on host machine with error **A2AMobiityServiceInstallerFailedWithMandatoryReboot (ID: 151081)**. Mobility service was uninstalled, but reboot was not performed on Azure VM."
<!--/issueDescription-->

## **Recommended Steps**

Reboot the host VM and retry the enable replication operation.
