<properties
	pageTitle="Operation Failure RCA"
	description="RCA - VM size not in zone"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="OperationFailure_RCA-VMSizeValidation-ZoneAllocationFailure"
	diagnosticScenario="OperationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We detected that the start operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the availability zone **<!--$zonenumber--> <!--/$zonenumber-->** does not have the capacity to support its allocation.<br>
<!--/issueDescription-->

The Azure Availability Zone did not have enough capacity to allocate the VM. Availability zones are physically separate locations within an Azure region that provide high availability to protect your applications and data from datacenter failures.<br>  

## **Recommended Steps**

Try the deployment again as the issue may have been temporary and there are now sufficient resources for the allocation. If that doesn't work, you have the following options:<br>

- Redeploy the VM to a new node in the existing availability zone.
- Resize the VM to a size that is currently available in your region. If you are using an older VM product, consider newer versions.
- Deploy a new VM to another availability zone in the region.
- Deploy a new VM in an Azure Availability Set.<br>

To determine available sizes in the Azure portal, select the VM and under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options.<br>

## **Recommended Documents**

To redeploy the VM in the availability zone:

- [Redeploy Windows virtual machine to new Azure node](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows)
- [Redeploy Linux virtual machine to new Azure node](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux)<br>

For determining sizes:

- For PowerShell, Use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command and filter for a region:<br>`Get-AzComputeResourceSku` &vert; `where {$_.Locations.Contains("<<insert-region>>")}`
- For Azure CLI, Use the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command with the `--location` parameter to filter for a region:<br>`az vm list-skus --location <<insert-region>> --output table`
- For REST API, use the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.<br>

For resizing:

- [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/) for a conceptual overview on working with VM sizes, availability sets, availability zones, and regions.
- [Resize a Windows VM not in an availability set](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-not-in-an-availability-set) to resize a VM that's not in an availability set using PowerShell.<br>






