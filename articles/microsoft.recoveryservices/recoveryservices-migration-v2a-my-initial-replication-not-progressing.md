<properties
    pageTitle="VMware to Azure - My Initial replication is not progressing"
    description="VMware to Azure - My Initial replication is not progressing"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680615"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="768a5733-ea50-4f62-8100-a66e9146fc45"
	ownershipId="Compute_SiteRecovery"
/>

# VMware/Physical to Azure - My Initial replication is not progressing

## **Recommended Steps**

### Critical process server

Unhealthy servers impacts replication of a virtual machine. Ensure associated process server is healthy. If not, [**troubleshoot all process server alerts**](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health).

### Critical configuration server

Ensure that associated configuration server is healthy and [**troubleshoot all configuration server alerts**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server).

### Connectivity

* Troubleshoot all [connectivity issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#step-2-troubleshoot-connectivity-and-replication-issues) to ensure smooth replication. If connectivity breaks, initial replication will not progress.
* Ensure all necessary folders are [excluded from antivirus software](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program)

### High churn

Ensure that the [data change rates/churn](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-high-churn-error-78188) is within the limits. High churn will lead to slow replication.

### Source machine heartbeat

Ensure that the mobility agent [heartbeat on source machine](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-no-heartbeat-error-78174) is latest for smooth replication.
