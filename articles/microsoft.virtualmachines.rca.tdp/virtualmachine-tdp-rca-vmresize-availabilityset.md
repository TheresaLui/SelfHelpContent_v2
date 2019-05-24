<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM size not in region"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-VMSizeValidation_NotInCluster"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We need some actions from you to deploy your resource

<!--issueDescription-->
We detected that the deployment for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the availability set **<!--$avsetname-->myAvailabilitySet<!--/$avsetname-->** must be reconfigured to include the VM size that you specified.<br>
<!--/issueDescription-->

You attempted to resize a VM to a size that is not available in its current availability set, as supported by the hardware cluster that supports the availability set. You have a couple of options:

- Choose a size that is included in your availability set.
- Choose a size that is not included in your availability set. However, you must first you must stop the VMs in the availability set. This is because Azure must have all the VMs deallocated in the set to reconfigure them to support the new size.<br> 

The following sections have PowerShell examples use these variables:

- Your resource group: `$myResourceGroup`
- Your virtual machine: `$myvM`
- New VM size: `$newSize`

## To resize to a currently supported size in the availability set

List the VM sizes that are available on the hardware cluster where the VM is hosted.

```powershell

Get-AzVMSize -ResourceGroupName $myResourceGroup -VMName $myVM
``` 
If the desired size is listed, resize the VM. 

```powershell

$vm = Get-AzVM -ResourceGroupName $myResourceGroup -VMName $myVM 
$vm.HardwareProfile.VmSize = $newSize
Update-AzVM -VM $vm -ResourceGroupName $myResourceGroup
```

## To resize a new size in the availability set

List the VM sizes that are available on the hardware cluster where the VM is hosted.
```powershell

Get-AzVMSize -ResourceGroupName $resourceGroup -VMName $vmName
```
Stop all VMs in the availability set.

```powershell

$as = Get-AzAvailabilitySet -ResourceGroupName $resourceGroup
$vmIds = $as.VirtualMachinesReferences
foreach ($vmId in $vmIDs){
    $string = $vmID.Id.Split("/")
    $vmName = $string[8]
    Stop-AzVM -ResourceGroupName $resourceGroup -Name $vmName -Force
  }
```

Resize and restart the VMs in the availability set.

```powershell

$as = Get-AzAvailabilitySet -ResourceGroupName $resourceGroup
$vmIds = $as.VirtualMachinesReferences
  foreach ($vmId in $vmIDs){
    $string = $vmID.Id.Split("/")
    $vmName = $string[8]
    $vm = Get-AzVM -ResourceGroupName $resourceGroup -Name $vmName
    $vm.HardwareProfile.VmSize = $newSize
    Update-AzVM -ResourceGroupName $resourceGroup -VM $vm
    Start-AzVM -ResourceGroupName $resourceGroup -Name $vmName
  }
```

## Resources

In addition to availability sets, consider Azure Availability Zones. Availability zones provide high availability by having VMs grouped in one or more physical locations within an Azure Region.<br>

| To learn about ... | See these articles |
| --- | --- |
| Availability Zones | [Azure Availability Zones](https://azure.microsoft.com/global-infrastructure/availability-zones/) |
| Availability sets compared with availability zones | [Azure VMs : Availability Sets and Availability Zones](https://social.technet.microsoft.com/wiki/contents/articles/51828.azure-vms-availability-sets-and-availability-zones.aspx) |
| Availability sets | [Tutorial: Create and deploy highly available virtual machines with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) |
| Manage availability sets for Windows VMs | [Manage the availability of Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) |
| Manage availability sets for Linux VMs | [Manage the availability of Linux virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/manage-availability) |



