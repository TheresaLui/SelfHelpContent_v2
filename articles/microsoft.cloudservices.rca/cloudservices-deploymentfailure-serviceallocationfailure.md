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

## **Diagnosis Details**

Following are the details specific to this Deployment failure:

* **Deployment operation time**: **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**

* **Name of the Virtual Machine**: **<!--$ResourceName-->virtualMachine<!--/$ResourceName-->**

* **Error Message**: The operation failed: 'The server encountered an internal error. Please retry the request.'

* **Cause of the failure**: If you are deploying into an existing VNet, Affinity Group, or Hosted Service, your deployment is **pinned** to a cluster which will cause all further deployment operations (like deploying to a different slot, scale up etc) to bound to the same cluster. This cluster might be full and cannot support any more capacity.

* **Action Plan (Please try the following)**:
  * Migrated the virtual machine to ARM

      For migrating to classic to ARM, please follow the below steps:
      Move classic resources to ARM before moving it to a different subscription. Refer to the following documents to move resources from classic to ARM:

      https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-plan?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json

      https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-deep-dive

      Steps to migrate using PowerShell: https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-ps 

  * Deploy to a new Cloud Service

    Delete VM, create a new VM and cloud service with the existing OS Disk.
    
  * Downsize the VM to check if the cluster can allocate the nodes.
  * Try again in the future. Capacity might become available. 

   (We recommend you to migrate the VM to ARM since classic infrastructure might get decommissioned in near future.)

* **Understanding Service Allocation Problem:**:

  In RDFE both the PaaS and IaaS offering run on a Cloud Service. The only difference is when re-create the PaaS/IaaS deployments and the overall Cloud Service concept is the same.

  A request to allocate deallocated VM or add a VM or a role instance to an existing cloud service has to be attempted at the original cluster that hosts the existing cloud service. Creating a new cloud service allows the Azure platform to find another cluster that has free resources or supports the VM size that you requested.

  For Classic VMs, they were pinned to a cluster where was having allocation issue. The allocation requests to restart these VMs have to be attempted at the original cluster that hosts the cloud service. Creating a new cloud service allows the Azure platform to find another cluster that has free resources or supports the VM size that you requested.

## **Recommended documents**
* [Troubleshooting allocation failure when you deploy Cloud Services in Azure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions) (Applicable to IaaS VM deployments)
* [Troubleshooting steps specific to allocation failure scenarios in the classic deployment model](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure-classic#resize-a-vm-or-add-vms-or-role-instances-to-an-existing-cloud-service)
