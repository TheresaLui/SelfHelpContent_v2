<properties
    pageTitle="Push installation fails because the boot is an EFI based partition"
    description="Push installation fails because the boot is an EFI based partition"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_BootOnEfiPartition"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push installation of mobility agent fails because boot is an EFI firmware

<!--issueDescription-->
Push installation fails because the boot is an EFI based partition on the source machine. This is an unsupported configuration.
<!--/issueDescription-->

## **Recommended Steps**

To protect a system with Azure Site Recovery, the virtual machine (VM) should be booted with BIOS as the firmware instead of EFI. To resolve the issue, change the configuration of the VM to boot with BIOS as the firmware.
