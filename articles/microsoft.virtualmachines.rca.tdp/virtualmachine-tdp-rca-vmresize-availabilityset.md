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

You attempted to resize a VM to a size that is not available in its current availability set. You have a couple of options:
- Choose a size that is included in your availability set.
- Resize the VM, but first you must stop the VMs in the availability set. This is because Azure must have all the VMs deallocated in the set to reconfigure them to support the new size.<br> 

### Resolutions

The PowerShell examples in this section use these variables:

- Your resource group: `$myResourceGroup`
- Your virtual machine: `$myvM`
- New VM size: `$newSize`

## To list available sizes in an availabity set

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

## To resize a VM in an availability set

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
