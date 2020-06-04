<properties
    pageTitle="Enable protection failed because device name isn’t UUID"
    description="Enable protection failed because device name isn’t UUID"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_MobilityAgentInstallFailure_GrubDeviceNameChange"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable protection failed because device name isn’t UUID

<!--issueDescription-->
The GRUB configuration files ("/boot/grub/menu.lst", "/boot/grub/grub.cfg", "/boot/grub2/grub.cfg" or "/etc/default/grub") may contain the value for the parameters root and resume as the actual device names instead of UUID. Site Recovery mandates UUID approach as devices name may change across reboot of the VM as VM may not come-up with the same name on failover. Therefore, this results in issues.
<!--/issueDescription-->

## **Recommended Steps**

The device names should be replaced with the corresponding UUID. To do that, follow the steps listed in [How to Fix](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#enable-protection-failed-as-device-name-mentioned-in-the-grub-configuration-instead-of-uuid-errorid-95320).
