<properties
    pageTitle="The GRUB configuration has the entry for the device which doesn't exist"
    description="The GRUB configuration has the entry for the device which doesn't exist"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_MobilityAgentInstallFailure_DeviceNotExist"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# The GRUB configuration has the entry for the device which doesn't exist

<!--issueDescription-->
The GRUB configuration has the entry for the device which doesn't exist.
<!--/issueDescription-->

## **Recommended Steps**

If the Logical Volume Manager (LVM) device doesn't exist, fix either by creating it or removing the parameters that indicate the LVM device being discovered at the time of booting from the GRUB configuration files, and then retry the enable protection.
