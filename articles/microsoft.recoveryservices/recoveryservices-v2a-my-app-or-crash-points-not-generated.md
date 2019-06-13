<properties
    pageTitle="VMware to Azure - My application or crash consistent points are not generated"
    description="VMware to Azure - My application or crash consistent points are not generated"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32642159"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public"
    articleId="d5a1c151-4e2c-45ba-9a3a-476e450d1487"
/>

# VMware/Physical to Azure - My application or crash consistent points are not generated

## Common pre-requisites

1. Unhealthy servers impacts replication of a virtual machine. Ensure associated process server is healthy. If not, [troubleshoot all process server alerts](https://aka.ms/health_ps_critical).
1. Ensure that associated configuration server is healthy and [troubleshoot all configuration server alerts](https://aka.ms/asr_cs_troubleshoot).
1. Troubleshoot all [connectivity issues](https://aka.ms/v2a_replication_connectivity)  to ensure smooth replication. If connectivity breaks, initial replication will not progress.
1. Ensure all necessary folders are [excluded from antivirus software](https://aka.ms/v2a_antivirus_exclusions).
1. Ensure that the mobility agent heartbeat on [source machine is latest](https://aka.ms/v2a_agent_heartbeat_TS) for smooth replication.

## Crash consistency points are not generated

1. Ensure all pre-requisites mentioned in the above section are validated.
1. High churn: Ensure that the [data change rates/churn](https://aka.ms/v2a_high_churn_TS) is within the limits. High churn will lead to slow replication and hinder crash consistent point generation.

## Application consistency points are not generated

1. Ensure all pre-requisites mentioned in the top section are validated.
1. Ensure that **Site Recovery VSS provider** is installed on the machine. If not, [complete installation](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures).
1. Ensure that **Site Recovery VSS provider** is running on the machine. If not, [start the services](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#missing-app-consistent-recovery-points-error-78144).

## **Recommended Documents**

1. **Known issue** in [SQL Server 2016 and 2017](https://support.microsoft.com/help/4493364)<br>
1. **Known issue** is [SQL Server instances with AUTO_CLOSE DBs](https://support.microsoft.com/help/4504104)<br>
1. **Known issue** in [SQL Server 2008 R2](https://support.microsoft.com/help/4504103)
