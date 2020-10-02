
<properties
    pageTitle="Troubleshooting High CPU for an Azure Virtual Machine"
    description="Troubleshooting High CPU for an Azure Virtual Machine"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="mahuss"
    displayOrder="0"
    articleId="024da352-807e-475b-b8ae-68f42be8d2b6"
    selfHelpType="Apollo"
    supportTopicIds="8b618100-f5cd-7ad5-1c69-72aaf37d801d"
    productPesIds="14749"
    resourceTags="windows"
    cloudEnvironments="public"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting High CPU for an Azure Virtual Machine

## **Troubleshooting High CPU Usage for an Azure Virtual Machine**

:::Section Metrics and Diagnostics:::

Review the graph to see the CPU usage as it correlates to your workload. Identify any patterns or spikes that are tied to the load, scheduled jobs, or unexpected consumption of resources.

<metric>
    <name>Percentage CPU</name>
    <aggregationType>Avg</aggregationType>
    <timeSpanDuration>1d</timeSpanDuration>
    <title>Current Virtual Machine CPU usage</title>
</metric>

## VM Performance diagnostics

We are attempting to run diagnostics for your Azure Virtual Machine. If any issues are detected, the findings will be listed below.

<Insight>
    <symptomId>HighCpuUsageAzurePortalInsight,VMPerfDiagExtAzurePortalInsight</symptomId>
    <executionText>We are running a few performance checks on your VM</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>false</additionalInputsReq>
</Insight>
