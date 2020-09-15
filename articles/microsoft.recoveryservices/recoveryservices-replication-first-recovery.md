<properties
    pageTitle="The first recovery point did not get generated"
    description="Questions or issues related to the first recovery point not being generated"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32745027"
    resourceTags=""
    productPesIds="16370"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8705922f-8944-4505-82bd-c559b591b6ee"
/>

# The first recovery point did not get generated

## **Recommended Documents**

- [Troubleshoot common Azure to Azure VM ongoing replication issues](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication)
- [Recovery points are not generating for the replicated VM](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#recovery-points-not-getting-generated)
- [Understand and resolve high data change rate/churn issue on the source virtual machine](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#high-data-change-rate-on-the-source-virtal-machine)
- [Troubleshoot COM+/Volume Shadow Copy service error (error code 151025)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#comvolume-shadow-copy-service-error-error-code-151025)
- [Check outbound connectivity to Site Recovery URLs or IP ranges from the VM](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors?#outbound-connectivity-for-site-recovery-urls-or-ip-ranges-error-code-151037-or-151072)
- [Troubleshoot all process server alerts](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health)
- [Troubleshoot all configuration server alerts](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server)
- [Troubleshoot all connectivity issues to ensure smooth replication](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#step-2-troubleshoot-connectivity-and-replication-issues)
- [Ensure all necessary folders are excluded from antivirus software](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program)
- [Ensure that the data change rates/churn is within the limits](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-high-churn-error-78188)
- [Ensure that the mobility agent heartbeat on source machine is latest for smooth replication.](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-no-heartbeat-error-78174)
- [Boot disk not found (Error 95310)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)
- [Multiple Boot disks found (Error 95311)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)
- [System and boot partitions/volumes on different disks (Error 95309)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)
- [To quickly unblock mobility agent installation failures, ensure push installation prerequisites for Windows  are met.](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-windows-computer)
- [To quickly unblock mobility agent installation failures, ensure push installation prerequisites for Windows  are met.](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-linux-server)
- [Credential/privilege errors (Error ID: 95107, 95108, 95517, 95518)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108)
- [Login failures (Error ID: 95519, 95520, 95521, 95522)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108)
- [Connectivity errors (Error ID: 95117, 95118)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#connectivity-failure-errorid-95117--97118)
- [File sharing, printer/WMI configuration errors (Error ID: 95105, 95106, 95103)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
- [VSS installation failures](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)
