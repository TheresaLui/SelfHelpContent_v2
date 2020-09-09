<properties
    pageTitle="Crash-consistent recovery points are not being generated"
    description="If you have missing crash-consistent points that you wanted to use in order to failover"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744976"
    resourceTags=""
    productPesIds="16370"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b15e001a-dddb-4ec1-ae7e-27b9d823c182"
/>

# Crash-consistent recovery points are not being generated

## **Recommended Documents**

- [Understand and resolve high data change rate/churn issue on the source virtual machine](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#high-data-change-rate-on-the-source-virtal-machine)
- [Troubleshoot COM+/Volume Shadow Copy service error (error code 151025)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#comvolume-shadow-copy-service-error-error-code-151025)
- [Check outbound connectivity to Site Recovery URLs or IP ranges from the VM](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors?#outbound-connectivity-for-site-recovery-urls-or-ip-ranges-error-code-151037-or-151072)
- [Steps to configure outbound network connectivity](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication#configure-outbound-network-connectivity)
- [Review the Support Requirements for all components](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix)
- [Steps to enable replication for Azure VMs](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication)
- [Networking guidance for replicating Azure virtual machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking)
- [Understand the scenario architecture and components](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture)
- [Troubleshoot all process server alerts](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health)
- [Troubleshoot all configuration server alerts](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server)
- [Troubleshoot all connectivity issues to ensure smooth replication](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#step-2-troubleshoot-connectivity-and-replication-issues)
- [Ensure all necessary folders are excluded from antivirus software](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program)
- [Ensure that the mobility agent heartbeat on source machine is latest for smooth replication](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-no-heartbeat-error-78174)
- [Known issue in SQL Server 2016 and 2017](https://support.microsoft.com/help/4493364/fix-error-occurs-when-you-back-up-a-virtual-machine-with-non-component)
- [Known issue is SQL Server instances with AUTO_CLOSE DBs](https://support.microsoft.com/help/4504104/non-component-vss-backups-such-as-azure-site-recovery-jobs-fail-on-ser)
- [Known issue in SQL Server 2008 R2](https://support.microsoft.com/help/4504103/non-component-vss-backup-fails-for-server-hosting-sql-server-2008-r2)
- [Ensure that the data change rates/churn is within the limits](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-high-churn-error-78188)
