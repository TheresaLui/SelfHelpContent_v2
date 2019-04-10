<properties
	pageTitle="cluster/notready"
	description="cluster/notready"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608953"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="6e869b56-8838-4e40-9f56-2556d3900b6d"
/>

# Cluster Not Ready

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Common questions and solutions for cluster nodes](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#nodes)<br>
* ["Out of disk space" warning](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#nodes)<br>
* [Application monitoring](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-overview#application-monitoring)<br>
* [Cluster monitoring](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-overview#platform-cluster-monitoring)<br>
* [Query EventStore to understand your cluster health](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-eventstore-query)<br>
* [EventStore sample queries](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-eventstore-query#sample-scenarios-and-queries)<br>
* [Check Service Fabric health monitoring](https://docs.microsoft.com/azure/service-fabric/service-fabric-health-introduction)<br>
* [Common issues during deployment](https://gooroo.io/GoorooTHINK/Article/17102/Azure-Service-Fabric-Cluster--Deployment-Issues)<br>
