<properties
	pageTitle="Allocation Failure RCA"
	description="Deployment Failure due to Pinned Cloud Service"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	articleId="deploymentfailure_rca-constrainedallocationfailed"
	diagnosticScenario="DeploymentFailure,"
	selfHelpType="rca"
	supportTopicIds="32565644,32565474,32565475,32565476,32565478,32565479,32565480"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for cloud service **<!--$csname-->cloud service<!--/$csname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to an allocation failure.

Microsoft Azure partitions compute nodes in a datacenter into various clusters, with each cluster containing about a thousand nodes/blades. The cloud services when deployed get pinned to a single cluster, and don’t currently span across multiple clusters. In some cases, as availability of free blades or free space within a blade in a cluster fluctuates, the constraints to find an allocation for the service may not be not met. When these constraints are not satisfied, we return back the request as a service allocation failure.
<!--/issueDescription-->

## **Details of the diagnosis**
Following are the details specific to this Deployment failure:

* **Deployment operation time**: **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**

* **Name of the Cloud Service**: **<!--$csname-->cloud service<!--/$csname-->**

* **Error Message**: Allocation failed; unable to satisfy constraints in request. The requested new service deployment is bound to an Affinity Group, or it targets a Virtual Network, or there is an existing deployment under this hosted service. Any of these conditions constraints the new deployment to specific Azure resources. Please retry later or try reducing the VM size or number of role instances. Alternatively, if possible, remove the aforementioned constraints or try deploying to a different region.

* **Cause of the failure**: If you are deploying into an existing VNet, Affinity Group, or Hosted Service, your deployment is **pinned** to a cluster which will cause all further deployment operations (like deploying to a different slot, scale up etc) to bound to the same cluster. This cluster might be full and cannot support any more capacity.

* **Possible mitigations**: Please try the following:
-	Remove the constraints that are binding you to the cluster (deploy to a different VNet, deploy to a new Cloud Service)
-	Lower your role instance count request. There might be capacity for a smaller deployment.
-	Try again in the future. Capacity might become available. 

## **Recommended Document**

* [Allocation Failures](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures)
