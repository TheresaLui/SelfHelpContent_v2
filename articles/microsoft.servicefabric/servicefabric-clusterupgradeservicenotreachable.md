<properties
	pageTitle="cluster/upgradeservicenotreachable"
	description="cluster/upgradeservicenotreachable"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608935"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="c04d7e62-3b60-4eb0-bac3-86067fedf102"
/>

# Upgrade Service Not Reachable

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

[Common questions and solutions for Service Fabric clusters](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster)<br>
[Why is my cluster upgrade taking so long?](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Why%20do%20cluster%20upgrades%20take%20so%20long.md)<br>
["Upgrade Service Unreachable" errors](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Cluster%20Not%20Reachable%20%20UpgradeServiceNotreachable.md)<br>
[Upgrade service architecture](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/FUS%20Stream%20Architecture.md)<br>
[Common causes for "Upgrade Service Unreachable" errors](https://stackoverflow.com/search?q=Service+Fabric+Upgrade+Service+unreachable)<br>
[Best Practices for Service Fabric clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-production-readiness-checklist)<br>
