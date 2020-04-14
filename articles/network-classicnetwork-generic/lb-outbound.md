<properties
	pageTitle="No outbound connectivity from Backend Pool"
	description="No outbound connectivity from Backend Pool"
	service="microsoft.network"
	resource="loadbalancers"
	authors="spacest"
  ms.author="mariliu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637533"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="lb-outbound"
	ownershipId="CloudNet_LoadBalancer"
/>


# Troubleshoot outbound connectivity from Backend Pool

Did you know: 8 of 10 "No outbound connectivity from backend pool" issues were solved using the resources below. 

## **Recommended Steps**

1.  Know the traffic flow. What is the source and destination, and what is in between? 
2. Check if there's any Network Security Group, User Defined Route, or any other filtering system which can block or alternate the outbound connectivity
3. Examine every hop to understand if the traffic is flowing as expected. Learn how to use [connection troubleshoot](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-portal).
4. Are you using an **internal Standard Load Balancer**? If yes, you need take steps to [create outbound connectivity](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-rules-overview#outbound-nat-for-internal-standard-load-balancer-scenarios) for the VMs in the backend pool if outbound connectivity is desired.
5. If this is an intermittent issue, does your application initiate many outbound flows and you experience [SNAT port exhaustion](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#problemsolving)?
6. If you're using a 3rd party network virtual appliance (NVA) from Azure Marketplace with Azure Load Balancer, make sure you have the instructions from NVA vendor and follow the instructions. See [Troubleshooting NVA devices](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva). 

## **Recommended Documents**

* [Outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)
* [Troubleshoot Azure Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot)
* [Metrics and health diagnostics for Standard Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics)
* [Azure Monitor logs for public Basic Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log#enable-logging)
