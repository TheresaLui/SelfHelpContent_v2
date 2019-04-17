<properties
	pageTitle="cluster/unhealthynodes"
	description="cluster/unhealthynodes"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608963"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="19e1fa7e-c328-4634-84be-653cc539bdd0"
/>

# Unhealthy Nodes

## Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters
As of Service Fabric runtime version 6.4.644 for Linux clusters a previous issue with with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Common questions and solutions for cluster nodes](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#nodes)<br>
* ["Out of disk space" warning](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#nodes)<br>
* [Cluster monitoring](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-overview#platform-cluster-monitoring)<br>
* [Query EventStore to understand your cluster health](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-eventstore-query)<br>
* [EventStore sample queries](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-eventstore-query#sample-scenarios-and-queries)<br>
* [Check Service Fabric health monitoring](https://docs.microsoft.com/azure/service-fabric/service-fabric-health-introduction)<br>
