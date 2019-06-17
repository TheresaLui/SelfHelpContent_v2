<properties
    pageTitle="VMware to Azure - My Initial replication is not progressing"
    description="VMware to Azure - My Initial replication is not progressing"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32642155"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public"
    articleId="1db0cf7f-e844-405c-9f67-5c7c6fe738db"
/>

# VMware/Physical to Azure - My Initial replication is not progressing

## **Recommended steps**

**Critical process server**

Unhealthy servers impacts replication of a virtual machine. Ensure associated process server is healthy. If not, [**troubleshoot all process server alerts**](https://aka.ms/health_ps_critical).

### Critical configuration server

Ensure that associated configuration server is healthy and [**troubleshoot all configuration server alerts**](https://aka.ms/asr_cs_troubleshoot).

### Connectivity

* Troubleshoot all [connectivity issues](https://aka.ms/v2a_replication_connectivity) to ensure smooth replication. If connectivity breaks, initial replication will not progress<br>
* Ensure all necessary folders are [excluded from antivirus software](https://aka.ms/v2a_antivirus_exclusions)

### High churn

Ensure that the [data change rates/churn](https://aka.ms/v2a_high_churn_TS) is within the limits. High churn will lead to slow replication.

### Source machine heartbeat

Ensure that the mobility agent [heartbeat on source machine](https://aka.ms/v2a_agent_heartbeat_TS) is latest for smooth replication.
