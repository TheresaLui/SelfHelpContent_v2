<properties
	pageTitle="cluster/clusterupgrade"
	description="cluster/clusterupgrade"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608946"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="f7d8df66-6bd3-4d84-81c8-a2bf560b7dc8"
/>

# Cluster Upgrades

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Common questions and solutions for cluster upgrades](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster)<br>
* [Troubleshoot cluster upgrade issues](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Troubleshooting%20failed%20Fabric%20Upgrade.md)<br>
* ["Upgrade Service Unreachable" error](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Cluster%20Not%20Reachable%20%20UpgradeServiceNotreachable.md)<br>
* [Service Fabric cluster upgrade concepts and settings](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-upgrade)<br>
* [Service Fabric standalone cluster upgrade](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-upgrade-windows-server)<br>
* [Tutorial: Upgrade the runtime of a Service Fabric cluster in Azure](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-upgrade-cluster)<br>
