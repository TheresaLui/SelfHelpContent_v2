<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - resource locked"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_DeploymentFailure_RCA-resource-locked"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32641079,32641082,32641076,32641075,32641080,32641074,32641076,32641077,32641072,32641073"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# We detected an operation on a locked resource

<!--issueDescription-->
We detected that the operation **<!--$OperationName-->operation<!--/$OperationName-->** on virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a scope lock **<!--$ScopeLock--> <!--/$ScopeLock-->** on the resource.<br>
<!--/issueDescription-->

To find the lock, select **Locks** on **Settings** blade for the resource, resource group, or subscription. You can delete the lock, or set its lock level to **CanNotDelete** or **ReadOnly**. If you do not see options to manage locks, you will need elevated rights to access them.<br>

See [Lock resources to prevent unexpected changes](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources) for detailed information included examples for applying and deleting locks using PowerShell, Azure CLI, and REST.
