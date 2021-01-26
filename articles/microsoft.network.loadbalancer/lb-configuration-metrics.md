<properties
	pageTitle="Azure Load Balancer configuration issues - how to set up metrics"
	description="Azure Load Balancer configuration issues - how to set up metrics"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781314"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="5deb7553-0965-45d3-a66d-895655a50a6k"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer Metrics

## **Recommended Steps**

* Multi-dimensional are not supported on Basic Load Balancer. To enable alerts for your load balancer, follow [these instructions](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard) to create a Standard SKU Load Balancer.
* Learn more about [multi-dimensional metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#multi-dimensional-metrics)
* Learn more about [how to view load balancer metrics on Azure Portal](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#view-your-load-balancer-metrics-in-the-azure-portal)
* Learn more about [common diagnostic scenarios and recommended views](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#common-diagnostic-scenarios-and-recommended-views)
* To see if data path of the load balancer is up and allowing traffic flow, check [data path availability metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#is-the-data-path-up-and-available-for-my-load-balancer-frontend)
* To see if backend instances are responding to probes, check [health probe status metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#are-the-backend-instances-for-my-load-balancer-responding-to-probes)
* Learn about how to troubleshoot inbound connectivity issues by using a combination of [data path availability and health probe status](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-diagnose-my-load-balancer-deployment).
* To see outbound connection statistics, check the [SNAT connection metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-outbound-connection-statistics)
* To see SNAT port usage and allocation, check [used SNAT Ports metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-snat-port-usage-and-allocation)
* To see inbound/outbound connection attempts, check [SYN packets metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-inboundoutbound-connection-attempts-for-my-service) 
* To see network bandwidth consumption, check [bytes and packet counters metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-network-bandwidth-consumption)
