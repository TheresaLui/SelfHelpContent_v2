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
	supportTopicIds=""
	resourceTags="AVS,privateClouds,vSAN"
	productPesIds="17080"
	cloudEnvironments="public"
	ownershipId="Azure_VMwareSolution_Content"
/>

# High vSAN Utilization Detected

## High vSAN Utilization
<!--issueDescription-->
vSAN has been reported as unhealthy at least once in the past 30 days. 

The capacity of the drives used for vSAN, besides the cache, is regarded as "vSAN Health". It is typically recommended that there be 25%-30% raw free disk space , or "slack-space", on the vSAN datastore in order to allow for expected host behavior (e.g., snapshots, maintenance, storage policy changes, etc.) and unexpected host behavior (e.g., failures). In this case, vSAN was reported as unhealthy because there was an instance where  "slack-space" was less than 30%. 
Note that vSAN usage greater than or equal to 80% is considered a breach of the SLA. 
<!--/issueDescription-->

## **Recommended Steps**
If vSAN usage is regularly high, then to increase raw free disk space, there are primarily two options:


1. Increase the size of vSAN datastore by adding a host, or hosts, if the private cloud is below the current limit of nodes per cluster. Here is a quick tutorial on how to do so: ["Tutorial: Scale an Azure VMware Solution private cloud"](https://docs.microsoft.com/azure/azure-vmware/tutorial-scale-private-cloud)
2. Purge data from the vSAN datastore.

If you believe the unhealthy vSAN is unrelated to normal use, please open a support request.

## **Recommended Documents**

* [Common questions about Azure VMware Solution](https://docs.microsoft.com/azure/azure-vmware/faq)
* [More on vSAN capacity management, from VMware](https://blogs.vmware.com/virtualblocks/2019/01/14/vsan-capacity-management-and-monitoring-part-1/)

