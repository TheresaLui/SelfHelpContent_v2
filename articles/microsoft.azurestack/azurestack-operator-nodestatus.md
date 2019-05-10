<properties
    pageTitle="Azure Stack Node status is adding"
    description="Azure Stack Node status permanent shows as adding"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="troettinger"
    ms.author="thoroet"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629188,32630575,32629232"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-operator-nodestatus"
/>

# Azure Stack Node status showing adding

An Azure Stack node keeps showing the operational status as “Adding” after a node operation like drain, resume, repair, shutdown or start was executed.
This can happen when the Fabric Resource Provider Role’s cache did not refresh after the node operation and is showing a wrong status. 

Applies to: Azure Stack build 1808, 1809 and 1811

## **Recommended Steps**

1. Open PowerShell and add your Azure Stack environment. (This requires Azure Stack PowerShell to be installed on your computer)
 <code>
Add-AzureRMEnvironment -Name AzureStack -armendpoint https://adminmanagement.local.azurestack.external
Add-AzureRMAccount -Environmentname AzureStack
</code>

2. Run the following command to restart the Fabric Resource Provider Role.
<code>
Restart-AzsInfrastructureRole -Name FabricResourceProvider
</code>

3. Validate the operational status of the impacted Scale Unit node changed to running. You can use the Admin Portal or the below PowerShell command:
<code>
Get-AzsScaleUnitNode |ft name,scaleunitnodestatus,powerstate
</code>

4. If the node operational status is still shown as “Adding” continue to open a support incident.


## **Recommended Documents**

- [Install Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure-stack/operator/azure-stack-powershell-install)
- [Monitor Add node operations](https://docs.microsoft.com/en-us/azure-stack/operator/azure-stack-add-scale-node#monitor-add-node-operations)