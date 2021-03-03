<properties
  pagetitle="Application consistent recovery points are not being generated"
  description="Missing app-consistent points that you wanted to use in order to failover"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sideeksh,sharrai"
  selfhelptype="Generic"
  supporttopicids="32744975"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="53ccadf1-b0a6-4cd5-a374-c90d901e6be0"
  ownershipid="Compute_SiteRecovery" />
# Application consistent recovery points are not being generated


## **Common issues and solutions**

- No app-consistent recovery point available for the VM in the past "X" minute.
    - Check some of the most common issues causing this error for – 
        - [Azure machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#error-id-153006---no-app-consistent-recovery-point-available-for-the-vm-in-the-past-x-minutes)
        - [VMware/Physical machines](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#error-id-78144---no-app-consistent-recovery-point-available-for-the-vm-in-the-last-xxx-minutes)
        - [Hyper-V machines](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#app-consistent-snapshot-issues)

    - If you are using a Linux operating system, then make sure you have [setup custom scripts](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#can-i-enable-replication-with-app-consistency-in-linux-servers) to create app-consistent recovery points.
    - Ensure that Volume Shadow Copy Services (VSS) are running and healthy on your source machines. Check the step-by-step guide for –
        - [Azure machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#vss-writer-is-not-installed---error-2147221164)
        - [VMware/Physical machines](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)
        - [Hyper-V machines](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot#vss-failing-inside-the-vm)
    - If the source machine is running any version of Microsoft SQL Server then check the documentation [here](https://docs.microsoft.com/troubleshoot/sql/admin/revocery-jobs-fail-servers) for a step by step guide on how to resolve this issue. For Microsoft SQL Servers 2008 or SQL Server 2008 R2 check the step-by-step guide [here](https://docs.microsoft.com/troubleshoot/sql/admin/asr-agent-vss-backup-fails).

- Replication is not progressing for the source machine.
    - Ensure that you have checked the supported [data churn limits](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#azure-site-recovery-limits) of Azure Site Recovery. A higher data churn will cause the replication to slow down. If the churn is high, then try to switch to a premium disk or reduce the churn.
    - For VMware/Physical machines, ensure that the configuration server and process server are in a healthy state and [all the services required for replication](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#step-2-check-process-server-services) are running. Also, make sure that the system time is in sync with the global time.

- Enable replication is failing for the source machine
    - If you’re trying to enable replication on encrypted Azure VMs, then make sure the [required key vault permissions](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-how-to-enable-replication-ade-vms#trusted-root-certificates-error-code-151066) are already present.
