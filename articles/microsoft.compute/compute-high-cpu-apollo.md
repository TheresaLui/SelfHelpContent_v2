
<properties
    pageTitle="Troubleshooting High CPU for an Azure Virtual Machine"
    description="Troubleshooting High CPU for an Azure Virtual Machine"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="mahuss"
    displayOrder="0"
    articleId="2fd4cdb3-6b23-40a9-8bf3-962351a7f4cc"
    selfHelpType="Apollo"
    supportTopicIds="8b618100-f5cd-7ad5-1c69-72aaf37d801d"
    productPesIds="14749"
    resourceTags="windows"
    cloudEnvironments="public"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting High CPU for an Azure Virtual Machine

## Troubleshooting High CPU Usage for an Azure Virtual Machine

This experience combines an automated performance check to detect anomalies in your Virtual Machine, shows metrics in real time, and provides troubleshooting steps to resolve any issues found.

:::Section Metrics and Diagnostics:::

### Metrics

The graph below shows the Virtual Machine CPU usage for the last 24 hours. Click on the chart to customize the view and/or update the filters. 

Please review the graph to see the CPU usage as it correlates to your workload. Identify any patterns or spikes that are tied to the load, scheduled jobs, or unexpected consumption of resources. 

<metric>
    <name>Percentage CPU</name>
    <aggregationType>Avg</aggregationType>
    <timeSpanDuration>1d</timeSpanDuration>
    <title>Current Virtual Machine CPU usage</title>
</metric>

### Diagnostics

We are attempting to run diagnostics for your Azure Virtual Machine. If any issues are detected, the findings will be listed below.

If your issue is happening currently, then this is the best time to review the captured data to attempt to locate the process leading to high CPU consumption. You can use the tools described in following recommendations for further troubleshooting.

<Insight>
    <symptomId>HighCpuUsageAzurePortalInsight,VMPerfDiagExtAzurePortalInsight</symptomId>
    <executionText>We are running a few performance checks on your VM</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>false</additionalInputsReq>
</Insight>
