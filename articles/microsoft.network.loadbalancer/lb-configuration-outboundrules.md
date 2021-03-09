<properties
	pageTitle="Azure Load Balancer Configuration Issues - Outbound Rules"
	description="Azure Load Balancer Configuration Issues - Outbound Rules"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781315"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6i"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer outbound rules configuration issues

## **Recommended Steps**

* Are you using Basic Load Balancer? SNAT ports are preallocated as described in [dynamic SNAT ports allocated](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#snatporttable). Create a [Standard Public Load Balancer](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard) with configurable SNAT port allocation to avoid SNAT exhaustion. 
* Consider the following options to avoid SNAT exhaustion when using a Standard Public Load Balancer: 
  1. [Scale outbound SNAT with multiple IP address](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#scale). Each of the IP address provides additional 64,000 ephemeral ports for Load Balancer to use as SNAT ports. 
  2. [Modify SNAT port allocation](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#scenarios-with-outbound-rules). You can use outbound rules to tune the automatic SNAT port allocation based on backend pool size.  
* If none of the preceding options suits your scenario, consider assigning Public IP to individual virtual machines. But note that this will expose the endpoints to the internet.  
* [Monitor SNAT port usage](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-snat-port-usage-and-allocation) and allocation on Azure Portal and [configure alerts](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#configure-alerts-for-multi-dimensional-metrics) accordingly to get alerts when SNAT port runs low. 
