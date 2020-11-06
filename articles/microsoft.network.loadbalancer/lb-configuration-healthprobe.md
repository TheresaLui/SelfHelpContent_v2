<properties
	pageTitle="Azure Load Balancer configuration issues - how to set up health probes"
	description="Azure Load Balancer configuration issues - how to set up health probes"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781311"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6k"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer health probes set up

## **Recommended Steps**

* A health probe is necessary to establish an inbound connection. Azure Load Balancer supports TCP listeners, HTTP endpoints, and HTTPS endpoints (only available for Standard SKU). ICMP is not supported. Learn more about [Azure Load Balancer health probes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview).
* Learn more about [design guidance for health probes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview#design)
* To see whether the health probe is probing for the backend instances, follow [these instructions](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#are-the-backend-instances-for-my-load-balancer-responding-to-probes) to view health probe health metrics on Azure Portal
