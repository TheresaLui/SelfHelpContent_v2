<properties
    pageTitle="VMware to Azure - My application or crash consistent points are not generated"
    description="VMware to Azure - My application or crash consistent points are not generated"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32642154"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d5a1c151-4e2c-45ba-9a3a-476e450d1487"
	ownershipId="Compute_SiteRecovery"
/>

# VMware/Physical to Azure - My application or crash consistent points are not generated

## **Recommended Steps**

### Common prerequisites

1. Unhealthy servers impacts replication of a virtual machine. Ensure associated process server is healthy. If not, [troubleshoot all process server alerts](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-process-server-health).
1. Ensure that associated configuration server is healthy and [troubleshoot all configuration server alerts](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server)
1. Troubleshoot all [connectivity issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#step-2-troubleshoot-connectivity-and-replication-issues) to ensure smooth replication. If connectivity breaks, initial replication will not progress
1. Ensure all necessary folders are [excluded from antivirus software](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program)
1. Ensure that the mobility agent heartbeat on [source machine is latest](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-no-heartbeat-error-78174) for smooth replication

### Crash consistency points are not generated

1. Ensure all pre-requisites mentioned in the above section are validated
1. High churn: Ensure that the [data change rates/churn](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#source-machines-with-high-churn-error-78188) is within the limits. High churn will lead to slow replication and hinder crash consistent point generation.

### Application consistency points are not generated

1. Ensure all pre-requisites mentioned in the top section are validated
1. Ensure that **Site Recovery VSS provider** is installed on the machine. If not, [complete installation](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures).
1. Ensure that **Site Recovery VSS provider** is running on the machine. If not, [start the services](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#missing-app-consistent-recovery-points-error-78144).

## **Recommended Documents**

* **Known issue** in [SQL Server 2016 and 2017](https://support.microsoft.com/help/4493364)<br>
* **Known issue** is [SQL Server instances with AUTO_CLOSE DBs](https://support.microsoft.com/help/4504104)<br>
* **Known issue** in [SQL Server 2008 R2](https://support.microsoft.com/help/4504103)
