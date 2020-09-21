<properties
    pageTitle="Troubleshooting High CPU for an Azure Virtual Machine"
    description="Troubleshooting High CPU for an Azure Virtual Machine"
    authors="timbasham"
    ms.author="mahuss"
    displayOrder=""
    articleId="2fd4cdb3-6b23-40a9-8bf3-962351a7f4cc"
    selfHelpType="Apollo"
        supportTopicIds="8b618100-f5cd-7ad5-1c69-72aaf37d801d"
        productPesIds="14749"
    cloudEnvironments="public"
    ownershipId="b6015c21-c91a-4248-8d13-426894cd5140"
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
    <symptomId>HighCpuUsageAzurePortalInsight</symptomId>
    <executionText>We are running a few performance checks on your VM</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>false</additionalInputsReq>
</Insight>

<Insight>
    <symptomId>VMPerfDiagExtAzurePortalInsight</symptomId>
    <executionText>We are running a few performance checks on your VM</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>false</additionalInputsReq>
</Insight>
