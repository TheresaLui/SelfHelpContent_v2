<properties
    pageTitle="VMware to Azure - My VM health is critical"
    description="VMware to Azure - My VM health is critical"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32642158"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public"
    articleId="91335914-b844-4952-a4b5-ae8098383586"
/>

# VMware/Physical to Azure - My VM health is critical

## **Recommended steps**

**Critical process server**

Unhealthy servers impacts replication of a virtual machine. Ensure associated process server is healthy. If not, [**troubleshoot all process server alerts**](https://aka.ms/health_ps_critical).

## Critical configuration server

Ensure that associated configuration server is healthy and [**troubleshoot all configuration server alerts**](https://aka.ms/asr_cs_troubleshoot).

## Connectivity

* Troubleshoot all [connectivity issues](https://aka.ms/v2a_replication_connectivity) to ensure smooth replication. If connectivity breaks, initial replication will not progress.
* Ensure all necessary folders are [excluded from antivirus software](https://aka.ms/v2a_antivirus_exclusions).

## High churn

Ensure that the [data change rates/churn](https://aka.ms/v2a_high_churn_TS) is within the limits. High churn will lead to slow replication.

## Source machine heartbeat

Ensure that the mobility agent [heartbeat on source machine](https://aka.ms/v2a_agent_heartbeat_TS) is latest for smooth replication.
