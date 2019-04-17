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

## **Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters**
As of Service Fabric runtime version 6.4.644 for Linux clusters a previous issue with with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

[Common questions and solutions for Service Fabric clusters](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster)<br>
[Why is my cluster upgrade taking so long?](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Why%20do%20cluster%20upgrades%20take%20so%20long.md)<br>
["Upgrade Service Unreachable" errors](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Cluster%20Not%20Reachable%20%20UpgradeServiceNotreachable.md)<br>
[Upgrade service architecture](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/FUS%20Stream%20Architecture.md)<br>
[Common causes for "Upgrade Service Unreachable" errors](https://stackoverflow.com/search?q=Service+Fabric+Upgrade+Service+unreachable)<br>
[Best Practices for Service Fabric clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-production-readiness-checklist)<br>
