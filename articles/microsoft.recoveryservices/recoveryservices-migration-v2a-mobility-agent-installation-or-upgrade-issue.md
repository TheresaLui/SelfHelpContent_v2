<properties
    pageTitle="VMware to Azure - Mobility agent installation or upgrade issue"
    description="VMware to Azure - Mobility agent installation or upgrade issue"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680613"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e454706c-a8f2-4f4c-bf93-be603d783a4c"
	ownershipId="Compute_SiteRecovery"
/>

# VMware/Physical to Azure - Mobility agent installation or upgrade issue

## **Recommended Steps**

### Prerequisites

* For smooth installation of mobility agent, ensure the push installation prerequisites for [Windows](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-windows-computer) and [Linux](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-linux-server) are met
* Ensure all Site Recovery folders are [excluded from antivirus](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program)

### Troubleshoot mobility agent installation failures

* Credential/privilege errors - [Error ID: 95107, 95108, 95517, 95518](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108)</br>
* Login failures - [Error ID: 95519, 95520, 95521, 95522](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#login-failures-errorid-95519-95520-95521-95522)</br>
* Connectivity errors - [Error ID: 95117, 95118](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#connectivity-failure-errorid-95117--97118)</br>
* File sharing, printer/WMI configuration errors - [Error ID: 95105, 95106, 95103](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)</br>
* Reboot warnings - [Error ID: 95265 & 95266](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#install-mobility-service-completed-with-warning-to-reboot-errorid-95265--95266)

### Supported/unsupported scenarios

* Is your workload on supported configuration to perform Disaster Recovery or migration? Ensure that the workload falls under our [support matrix](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix)</br>
* **Windows Server 2019** Operating System can be protected by Azure Site Recovery version 9.22. Follow [these guidelines](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to#between-an-on-premises-vmware-or-physical-site-to-azure) to upgrade your Site Recovery components</br>
* If the OS disk is a dynamic disk, it is not supported. [Data disk can be a dynamic disk](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#storage)</br>
* [Unsupported operating systems](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#unsupported-operating-systems)

## **Recommended Documents**

### Unsupported Boot configurations

* Boot disk not found - [Error 95310](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309
* Multiple Boot disks found - [Error 95311](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)
* System and boot partitions/volumes on different disks - [Error 95309](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)
* ASR [VSS installation failures](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)
