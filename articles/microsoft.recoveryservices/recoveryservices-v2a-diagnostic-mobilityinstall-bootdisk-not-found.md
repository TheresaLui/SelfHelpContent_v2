<properties
    pageTitle="The boot disk is not found"
    description="The boot disk is not found"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_MobilityAgentInstallFailure_BootDiskNotFound"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# The boot disk is not found

<!--issueDescription-->
When you run the fdisk command, you can see the output doesn't contain a single partition with bootable flag set. This is an unsupported configuration.
<!--/issueDescription-->

## **Recommended Steps**

1. For 9.20 or a later version of Site Recovery components, mount the boot partition on /boot
2. For versions before 9.20, to fix this issue, follow these steps:

    - Search for the partition that is mounted on /boot. If nothing is mounted on /boot and /boot contains the images of initrd or initramfs and kernel (vmlinuz* files), then search for the partition that is mounted on "/". This partition is the boot disk.
    - Run the fdisk command on the full disk that contains this partition. For example: "fdisk /dev/sda".
    - Input "a" and then press Enter key
    - The command window prompts for partition number. Then, pass the partition number of the boot disk like "1" and press Enter key.
    - Input "w" and then press Enter key to exit
    - Restart the enable protection job
