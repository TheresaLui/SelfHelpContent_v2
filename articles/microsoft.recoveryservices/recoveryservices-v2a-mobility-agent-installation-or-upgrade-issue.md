<properties
    pageTitle="VMware to Azure - Mobility agent installation or upgrade issue"
    description="VMware to Azure - Mobility agent installation or upgrade issue"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32642153"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public"
    articleId="6d233d9d-675d-413b-8ed6-589156fa5b6d"
/>

# VMware/Physical to Azure - Mobility agent installation or upgrade issue

## Prerequisites

* For smooth installation of mobility agent, ensure push installation prerequisites for [Windows](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-windows-computer) and [Linux](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-linux-server) are met.</br>
* Ensure all Site Recovery folders are [excluded from antivirus](https://aka.ms/asr_antivirus_exclusions)

### Troubleshoot mobility agent installation failures

* Credential/privilege errors - [Error ID: 95107, 95108, 95517, 95518](https://aka.ms/installation_credential_failures)</br>
* Login failures - [Error ID: 95519, 95520, 95521, 95522](https://aka.ms/installation_login_failures)</br>
* Connectivity errors - [Error ID: 95117, 95118](https://aka.ms/installation_connectivity_failures)</br>
* File sharing, printer/WMI configuration errors - [Error ID: 95105, 95106, 95103](https://aka.ms/installation_File_printer_failures)</br>
* Reboot warnings - [Error ID: 95265 & 95266](https://aka.ms/v2a_reboot_warnings)

### Supported/unsupported scenarios

* Is your workload on supported configuration to perform Disaster Recovery or migration? Ensure that the workload falls under our [support matrix](https://aka.ms/asr_v2a_support_matrix)</br>
* **Windows Server 2019** Operating System can be protected by Azure Site Recovery version 9.22. Follow [these guidelines](https://aka.ms/asr_vmware_upgrades) to upgrade your Site Recovery components</br>
* If the OS disk is a dynamic disk, it is not supported. [Data disk can be a dynamic disk](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#storage)</br>
* [Unsupported operating systems](https://aka.ms/ASR_unsupported_OS)

## **Recommended Documents**

### Unsupported Boot configurations

* Boot disk not found - [Error 95310](https://aka.ms/asr_boot_failures) </br>
* Multiple Boot disks found - [Error 95311](https://aka.ms/asr_boot_failures)</br>
* System and boot partitions/volumes on different disks - [Error 95309](https://aka.ms/asr_boot_failures)</br>
* ASR [VSS installation failures](https://aka.ms/asr_vss_installation_failures)
