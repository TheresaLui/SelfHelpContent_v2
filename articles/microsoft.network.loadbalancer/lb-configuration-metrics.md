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
* Multi-dimensional are not supported on Basic Load Balancer. To enable alerts for your load balancer, follow [instructions](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard) to create a Standard SKU Load Balancer.
* Learn more about list of [multi-dimensional metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#multi-dimensional-metrics) that are available. 
* Learn more about how to view load balancer metrics on [Azure Portal](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#view-your-load-balancer-metrics-in-the-azure-portal).
* Learn more about common diagnostic scenarios and recommended views[when to use which metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#common-diagnostic-scenarios-and-recommended-views)
1. To see if data path of the load balancer is up and allowing traffic flow, check [data path availability metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#is-the-data-path-up-and-available-for-my-load-balancer-frontend)
2. To see if backend instances are responding probes, check [health probe status metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#are-the-backend-instances-for-my-load-balancer-responding-to-probes)
3. Learn about how to troubleshooting inbound connectivity issue, use a combination of [data path availability and health probe status](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-diagnose-my-load-balancer-deployment).
3. To see outbound connection statistics, check the [SNAT connection metrics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-outbound-connection-statistics)
4. To see SNAT port usage and allocation, check [Used SNAT Ports metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-snat-port-usage-and-allocation)
5. To see inbound/outbound connection attempts, check [SYN packets metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-inboundoutbound-connection-attempts-for-my-service) 
6. To see network bandwidth consumption, check [bytes and packet counters metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-check-my-network-bandwidth-consumption)


