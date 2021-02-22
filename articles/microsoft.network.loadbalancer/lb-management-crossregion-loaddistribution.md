<properties
	pageTitle="Azure Load Balancer Management Issues - Load Distribution Issues with Cross-region Load Balancer"
	description="Azure Load Balancer Management Issues - Cannot delete load balancer"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32750781"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-1965-45d3-a66d-895655a50a6d"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Cross-region Load Balancer Distribution Issues

## **Recommended Steps**

* Verify that packets are going to the undesired region by checking [network bandwidth consumption](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-network-bandwidth-consumption) on Regional Load Balancer in the backend pool of the Cross-region Load Balancer.
* Compare latency between source regions with each destination region that is used by the Cross-region Load Balancer while making decisions concerning load distribution.
1. Review [latency data](https://docs.microsoft.com/azure/networking/azure-network-latency#september-2020-round-trip-latency-figures) based on source region and destination region. The source region is the [participating region](https://docs.microsoft.com/azure/load-balancer/cross-region-overview#participating-regions) that most of the client traffic falls under. The destination region is the region that each regional Load Balancer is deployed in.
2. Compare the latency data. Traffic should be sent to the destination region with lower latency value.
