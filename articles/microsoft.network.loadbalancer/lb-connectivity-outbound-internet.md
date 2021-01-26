<properties
	pageTitle="Azure Load Balancer Outbound Connectivity - Cannot Connect To Internet"
	description="Azure Load Balancer Outbound Connectivity - Cannot Connect To Internet"
	service="microsoft.network"
	resource="loadbalancers"
	authors="anavinahar"
	ms.author="anavin"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781326"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6f"
	ownershipId="CloudNet_LoadBalancer"
/>

# No outbound connectivity to the Internet
Did you know: 8 of 10 "No outbound connectivity from backend pool" issues were solved using the resources below.

## **Recommended Steps**

1.  Know the traffic flow. What is the source and destination, and what is in between? 
2. Check if there's any Network Security Group, User Defined Route, or any other filtering system that can block or alternate the outbound connectivity
3. Examine every hop to understand if the traffic is flowing as expected. Learn how to use [connection troubleshoot](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-portal).
4. Are you using an **internal Standard Load Balancer**? If yes, you need take steps to [create outbound connectivity](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-rules-overview#outbound-nat-for-internal-standard-load-balancer-scenarios) for the VMs in the backend pool, you want outbound connectivity.
5. If this is an intermittent issue, does your application initiate many outbound flows and do you experience [SNAT port exhaustion](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#problemsolving)?
6. If you're using a third-party network virtual appliance (NVA) from Azure Marketplace with Azure Load Balancer, make sure you have the instructions from NVA vendor and follow the instructions. See [Troubleshooting NVA devices](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva). 

## **Recommended Documents**

* [Outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)
* [Troubleshoot Azure Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot)
* [Metrics and health diagnostics for Standard Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics)
* [Azure Monitor logs for public Basic Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log#enable-logging)
