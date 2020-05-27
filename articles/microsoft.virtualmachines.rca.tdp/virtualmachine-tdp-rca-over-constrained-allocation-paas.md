<properties
	pageTitle="Allocation Failure RCA"
	description="RCA - rca-over-constrained-allocation-paas"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-over_constrained_allocation_paas"
	diagnosticScenario="DeploymentFailure,"
	selfHelpType="rca"
	supportTopicIds="32565644,32565474,32565475,32565476,32565478,32565479,32565480"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for cloud service **<!--$csname-->cloud service<!--/$csname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to an allocation failure.

Microsoft Azure partitions compute nodes in a datacenter into various clusters, with each cluster containing about a thousand nodes/blades. The cloud services when deployed get pinned to a single cluster, and don’t currently span across multiple clusters. In some cases, as availability of free blades or free space within a blade in a cluster fluctuates, the constraints to find an allocation for the service may not be not met. When these constraints are not satisfied, we return back the request as a service allocation failure.
<!--/issueDescription-->

## **Recommended Steps**

This issue commonly happens in one of the following scenarios:

* **Region Not Supported**: The virtual machine size requested in the deployment is not supported in the selected region. Check available VM sizes per region [here](https://azure.microsoft.com/global-infrastructure/services/).
* **Updating Pinned Cloud Service**: If a cloud service has a deployment in either slot, then the entire cloud service is pinned to a specific cluster. This means that if a deployment already exists in the production slot, then a new staging deployment can only be allocated in the same cluster as the production slot.
* **Scaling**: Adding new instances to an existing cloud service must allocate in the same cluster. Small scaling requests can usually be allocated, but not always.
* **Changing VM size or Adding new VM size**: The cluster your Cloud Service is pinned to might not have the required combination of VM sizes

The following are a few possible solutions you can try when encountering an allocation failure:

* For "Region Not Supported" try deploying in a different region or use VM sizes which are supported in the desired region
* For all other causes try these options:

	1. **The ideal solution with zero downtime is to create a new cloud service in the same region and then deploy your service into that new cloud service. See [here](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions) for more details.**<br>
	2. Retry the deployment later. There might have been enough resources freed up on the cluster to allow the deployment or scaling request to succeed. This is the easiest option, but there is no assurance that the deployment will succeed later. <br>
	3. Delete both the production and staging slots from your cloud service, which will unpin the cloud service from a cluster, and then redeploy into that same cloud service. This will incur down time.<br>
	4. If redeploying doesn't work then you may be trying to deploy a combination of VM sizes that aren't supported in a single cluster. In this case, you should try to use the VM size supported by cluster where your cloud service is pinned. <br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>

## **Recommended Documents**

* [Allocation Failures](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures)
