<properties
    pageTitle="How do you delete a scale set extension"
    description="How do you delete a scale set extension"
    service="scalesets"
    author="negat"
    displayOrder="43"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do you delete a scale set extension?


Here is an example using PowerShell:

```powershell
$vmss = Get-AzureRmVmss -ResourceGroupName "resource_group_name" -VMScaleSetName "vmssName" 

$vmss=Remove-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name "extensionName"

Update-AzureRmVmss -ResourceGroupName "resource_group_name" -VMScaleSetName "vmssName" -VirtualMacineScaleSet $vmss
```
 
The extensionName can be found in `$vmss`.
   