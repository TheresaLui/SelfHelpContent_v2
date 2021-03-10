<properties
	pageTitle="High vSAN Utilization Detected"
	description="vSAN utilization was detected recently as near or above the SLA threshold."
	infoBubbleText="High vSAN Utilization Detected. See details on the right."
	service="microsoft.AVS"
	resource="privateClouds"
	ms.author="michaelbarta"
	displayOrder=""
	articleId="highvsanutilization_b53b92be-32dc-4c13-ab13-238d6256d72a"
	diagnosticScenario="CheckVsanHealthInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32739946, 32739976, 32739979"
	resourceTags="AVS,privateClouds,vSAN"
	productPesIds="17080"
	cloudEnvironments="public"
	ownershipId="Azure_VMwareSolution_Content"
/>

# High vSAN Usage Detected

## High vSAN Usage
<!--issueDescription-->
Recently, vSAN datastore was reported as unhealthy. 

Excluding the cache, capacity of the drives used for the vSAN is termed as "vSAN health." We generally recommend 25%-30% raw free disk space, or *slack space,* on the vSAN datastore to allow for expected host behavior (for example, snapshots, maintenance, storage policy changes) and unexpected host behavior (such as failures). In this case, vSAN was reported as unhealthy because, in a recent instance the slack space was less than 30%. 

**Note:** vSAN usage greater than or equal to 80% is considered a breach of the SLA. 
<!--/issueDescription-->

## **Recommended Steps**

If vSAN usage is regularly high, consider increasing raw free disk space. To do this, use one of the two following options:

1. Increase the size of vSAN datastore by adding a host, or hosts, if the private cloud is below the current limit of nodes per cluster. For quick guidance, see ["Tutorial: Scale an Azure VMware Solution private cloud"](https://docs.microsoft.com/azure/azure-vmware/tutorial-scale-private-cloud).
2. Purge data from the vSAN datastore

If you think that the unhealthy vSAN is unrelated to normal use, open a support request.

## **Recommended Documents**

* [Common questions about Azure VMware Solution](https://docs.microsoft.com/azure/azure-vmware/faq)
* [More on vSAN capacity management, from VMware](https://blogs.vmware.com/virtualblocks/2019/01/14/vsan-capacity-management-and-monitoring-part-1/)

