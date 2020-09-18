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
	supportTopicIds="32565644,32565474,32569897,32565476,32565478,32565479"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for cloud service <!--$csname-->cloud service<!--/$csname--> initiated at <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) failed due to an allocation failure with error message: <br>

Allocation failed; unable to satisfy constraints in request. The requested new service deployment is bound to an Affinity Group, or it targets a Virtual Network, or there is an existing deployment under this hosted service.

The servers in Azure datacenters are partitioned into clusters. The Cloud Services when deployed for the first time gets pinned to a single cluster, and don’t currently span across multiple clusters. This will also cause all further deployment operations like deploying to a different slot, scale up etc to bound to the same cluster. In some cases, as capacity fluctuates, the constraints to find the required hardware may not be met on that cluster and we return back the request as a service allocation failure.
<!--/issueDescription-->

## **Recommended Steps**

We apologize for any inconvenience this may have caused you. We are actively working on improving the platform to not be limited to one cluster and make more resources available for your service needs. Meanwhile, there are a few options depending on your flexibility:<br>

- Redeploy to a new cloud service. This solution is likely to be most successful as it allows the platform to choose from all clusters in that region.
- Delete both production and staging slots. This solution will preserve your existing DNS name, but will cause downtime to your application.
- Use a Reserved IP. This solution will preserve your existing IP address, but will cause downtime to your application.
- Remove affinity group for new deployments. Affinity Groups are no longer recommended. Follow steps for #1 above to deploy a new cloud service. Ensure cloud service is not in an affinity group<br>

## **Recommended Documents**

- [How Allocation works](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#background--how-allocation-works)<br>
- [Why Allocation failures happen](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#why-allocation-failure-happens)<br>
- [Common scenarios for Allocation failure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#common-issues)<br>
- [Possible solutions for Allocation failure](https://docs.microsoft.com//azure/cloud-services/cloud-services-allocation-failures#solutions)<br>
