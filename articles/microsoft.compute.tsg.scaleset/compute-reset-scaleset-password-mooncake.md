<properties
    pageTitle="How do I reset the password or ssh key on my scale set VMs"
    description="How do I reset the password or ssh key on my scale set VMs"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    authors="scottAzure"
    ms.author="scotro"
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="MoonCake"
    articleId="compute-reset-scaleset-password-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# How do I reset the password or ssh key on my scale set VMs

To reset the password or ssh key used to authenticate to your scale set VMs, you must use either the VMAccessAgent extension (for Windows-based scale sets) or the VMAccessForLinux extension (for Linux-based scale sets).

## **Recommended Documents**

For more information, refer to [this document](https://docs.azure.cn/virtual-machines/extensions/vmaccess) that describes how to use the VMAccessForLinux extension for Linux-based scale sets. For Windows-based scale sets, here is sample powershell code:

```
$vmssName = "myvmss"
$vmssResourceGroup = "myvmssrg"
$publicConfig = @{"UserName" = "user"}
$privateConfig = @{"Password" = "********"}
$extName = "VMAccessAgent"
$publisher = "Microsoft.Compute"
$vmss = Get-AzureRmVmss -ResourceGroupName $vmssResourceGroup -VMScaleSetName $vmssName
$vmss = Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $extName -Publisher $publisher -Setting $publicConfig -ProtectedSetting $privateConfig -Type $extName -TypeHandlerVersion "2.0" -AutoUpgradeMinorVersion $true
Update-AzureRmVmss -ResourceGroupName $vmssResourceGroup -Name $vmssName -VirtualMachineScaleSet $vmss
```
