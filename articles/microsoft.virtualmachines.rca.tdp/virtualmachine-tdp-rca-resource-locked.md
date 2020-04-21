<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - resource locked"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-resource-locked"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We detected an operation on a locked resource

<!--issueDescription-->
We detected that the operation **<!--$OperationName-->operation<!--/$OperationName-->** on virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a scope lock **<!--$ScopeLock--> <!--/$ScopeLock-->** on the resource.<br>
<!--/issueDescription-->

To find the lock, select **Locks** on **Settings** blade for the resource, resource group, or subscription. You can delete the lock, or set its lock level to **CanNotDelete** or **ReadOnly**. If you do not see options to manage locks, you will need elevated rights to access them.<br>

See [Lock resources to prevent unexpected changes](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources) for detailed information included examples for applying and deleting locks using PowerShell, Azure CLI, and REST.



