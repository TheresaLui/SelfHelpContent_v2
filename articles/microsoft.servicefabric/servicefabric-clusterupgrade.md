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

## Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters

As of Service Fabric runtime version 6.4.644 for Linux clusters, a previous issue with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Common questions and solutions for cluster upgrades](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster)<br>
* [Troubleshoot cluster upgrade issues](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Troubleshooting%20failed%20Fabric%20Upgrade.md)<br>
* ["Upgrade Service Unreachable" error](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Cluster%20Not%20Reachable%20%20UpgradeServiceNotreachable.md)<br>
* [Service Fabric cluster upgrade concepts and settings](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-upgrade)<br>
* [Service Fabric standalone cluster upgrade](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-upgrade-windows-server)<br>
* [Tutorial: Upgrade the runtime of a Service Fabric cluster in Azure](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-upgrade-cluster)<br>
