<properties
	pageTitle="Service Allocation Failure RCA"
	description="Deployment Failure due to capacity of Pinned Cloud Service cluster"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="Microsoft.ClassicCompute"
	resource="virtualMachines"
	authors="zihzhan"
	ms.author="zihzhan"
	displayOrder=""
  	articleId="cloudservices-deploymentfailure-serviceAllocationFailure"
	diagnosticScenario="DeploymentFailure,"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for classic Virtual Machine **<!--$ResourceName-->virtualMachine<!--/$ResourceName-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to a Service Allocation Failure.
<!--/issueDescription-->

The servers in Azure datacenters are partitioned into clusters. The Classic Virtual Machine when deployed gets pinned to a single cluster, and doesn’t span across multiple clusters. In some cases, as capacity fluctuates, the constraints to find an allocation for the service may not be met. When these constraints are not satisfied, customers experience service allocation failures.

## **Recommended Steps**

We apologize for the inconvenience. You have the following options:  

* Migrate the IaaS classic virtual machine resources to Azure Resource Manager using the steps outlined in:
  
    - [Azure CLI commands to migrate](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-cli#step-1-prepare-for-migration)
    - [Azure PowerShell commands to migrate](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-ps#step-1-plan-for-migration)
    - [Azure Portal to migrate](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-overview#migration-of-storage-accounts)

* Consider [planning your migration to ARM](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-plan#plan)
* Copy the VM’s disks and use them to create a new VM instance (i.e. clone/copy VM) with the same data as the original VM instance
* Downsize the VM to check if the cluster can allocate the VM

If you still encounter a **Service Allocation Failure**, please consider using a different VM size, or deploying to another location.

## **Recommended Documents**

* [Common Errors when migrating from Classic VM to ARM VM](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-errors)
* [Troubleshooting allocation failure when you deploy Cloud Services in Azure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions)
* [Troubleshooting steps specific to allocation failure scenarios in the classic deployment model](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure-classic#resize-a-vm-or-add-vms-or-role-instances-to-an-existing-cloud-service)
