<properties
    pageTitle="Application consistent recovery points are not being generated"
    description="Missing app-consistent points that you wanted to use in order to failover"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744975"
    resourceTags=""
    productPesIds="16370"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="53ccadf1-b0a6-4cd5-a374-c90d901e6be0"
/>

# Application consistent recovery points are not being generated

## **Recommended Documents**

- [Troubleshoot common application consistent points not generating issues](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#error-id-153006---no-app-consistent-recovery-point-available-for-the-vm-in-the-last-xxx-minutes)
- [Application consistent points are not generating for SQL 2008/ 2008 R2](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#cause-1-known-issue-on-sql-server-20082008-r2)
- [Application consistent points are not generating for any SQL version with AUTO_CLOSE DBs](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#cause-2-azure-site-recovery-jobs-fail-on-servers-hosting-any-version-of-sql-server-instances-with-auto_close-dbs)
- [Application consistent points are not generating for VMs having Storage Spaces Direct](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#cause-3-you-are-using-storage-spaces-direct-configuration)
- [Troubleshoot Application consistent points not generating due to VSS issues](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#more-causes-due-to-vss-related-issues)
- [Steps to configure outbound network connectivity](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication#configure-outbound-network-connectivity)
- [Review the Support Requirements for all components](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix)
- [Steps to enable replication for Azure VMs](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication)
- [Networking guidance for replicating Azure virtual machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking)
- [Understand the scenario architecture and components](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture)
- [Ensure that Site Recovery VSS provider is installed on the machine. If not, complete installation.](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)
- [Ensure that Site Recovery VSS provider is running on the machine. If not, start the services.](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#missing-app-consistent-recovery-points-error-78144)
- [Known issue in SQL Server 2016 and 2017](https://support.microsoft.com/help/4493364/fix-error-occurs-when-you-back-up-a-virtual-machine-with-non-component)
- [Known issue is SQL Server instances with AUTO_CLOSE DBs](https://support.microsoft.com/help/4504104/non-component-vss-backups-such-as-azure-site-recovery-jobs-fail-on-ser)
- [Known issue in SQL Server 2008 R2](https://support.microsoft.com/help/4504103/non-component-vss-backup-fails-for-server-hosting-sql-server-2008-r2)
