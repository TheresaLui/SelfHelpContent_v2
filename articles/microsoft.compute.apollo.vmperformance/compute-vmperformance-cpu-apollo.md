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

## Troubleshooting High CPU for an Azure Virtual Machine
This experience integrates automated checks to detect high CPU consumption in your Virtual Machine and guides you with the troubleshooting steps.

:::Section Recommended Solution:::

<metric>
    <name>Percentage CPU</name>
    <aggregationType>Avg</aggregationType>
    <timeSpanDuration>1d</timeSpanDuration>
    <title>Current Virtual Machine CPU usage</title>
</metric>

<Insight>
    <symptomId>HighCpuUsageAzurePortalInsight,VMPerfDiagExtAzurePortalInsight</symptomId>
    <executionText>We are running a few performance checks on your VM</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>false</additionalInputsReq>
</Insight>
