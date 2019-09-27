<properties
	pageTitle="Service Allocation Failure RCA"
	description="Deployment Failure due to capacity of Pinned Cloud Service cluster"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="Microsoft.ClassicCompute"
	resource="virtualMachines"
	authors="ZihanZhang"
	ms.author="zihzhan"
	displayOrder=""
  articleId="cloudservices-deploymentfailure-serviceAllocationFailure"
	diagnosticScenario="DeploymentFailure,"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for classic Virtual Machine **<!--$ResourceName-->virtualMachine<!--/$ResourceName-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to an Service Allocation Failure issue.

The servers in Azure datacenters are partitioned into clusters. The classic virtual Machine when deployed get pinned to a single cluster, and don’t currently span across multiple clusters. In some cases, as capacity fluctuates, the constraints to find an allocation for the service may not be met. When these constraints are not satisfied, we return back the request as a service allocation failure.
<!--/issueDescription-->

## **Recommended Steps**

Please try the following **Action Plans** to address this Deployment failure:  
(We recommend you to **migrate the VM to ARM** since classic infrastructure might get decommissioned in near future.)

  * Migrated the virtual machine to ARM

    While there are plenty of amazing features and better supporting offered in Azure Resource Manager. It is recommended to ask Customers to [Plan out Migration to ARM](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-plan#plan).

    These steps show you how to use [Azure PowerShell commands to migrate](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-ps#step-1-plan-for-migration) infrastructure as a service (IaaS) resources from the classic deployment model to the Azure Resource Manager deployment model.

    Customers can also migrate resources by using the [Azure Command Line Interface (Azure CLI)](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-cli#step-1-prepare-for-migration).

    If Customers encounter issues during the migration, here is a [Common Errors Mitigations](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-errors) documents that can help.
    

  * **Re-deploy your VM to new cloud service.** The allocation requests to restart these VMs have to be attempted at the original cluster that hosts the cloud service. Creating a new cloud service allows the Azure platform to find another cluster that has free resources or supports the VM size that you requested. Hence, re-create the VM in a different cloud service will forces the VM to be allocated in the best cluster that have available nodes. 

    * For PaaS VM Instances. Delete the production and staging slots of an existing cloud service so that the cloud service is empty, and then **Create a new deployment in the existing cloud service**. This will re-attempt to allocation on all clusters in the region. Ensure the cloud service is not tied to an affinity group.

    * For IaaS Classic VM. Copy the VM’s disks and use them to create a new VM instance (i.e. clone/copy VM) with the same data as the original VM instance.
    
  * Downsize the VM to check if the cluster can allocate the nodes.
  * Try again in the future. Capacity might become available. 

**Understanding Service Allocation Problem:**:

  In RDFE both the PaaS and IaaS offering run on a Cloud Service. The only difference is when re-create the PaaS/IaaS deployments and the overall Cloud Service concept is the same.

  A request to allocate deallocated VM or add a VM or a role instance to an existing cloud service has to be attempted at the original cluster that hosts the existing cloud service. Creating a new cloud service allows the Azure platform to find another cluster that has free resources or supports the VM size that you requested.

  For Classic VMs, they were pinned to a cluster where was having allocation issue. The allocation requests to restart these VMs have to be attempted at the original cluster that hosts the cloud service. Creating a new cloud service allows the Azure platform to find another cluster that has free resources or supports the VM size that you requested.

## **Recommended documents**
* [Troubleshooting allocation failure when you deploy Cloud Services in Azure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions) (Applicable to IaaS VM deployments)
* [Troubleshooting steps specific to allocation failure scenarios in the classic deployment model](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure-classic#resize-a-vm-or-add-vms-or-role-instances-to-an-existing-cloud-service)
