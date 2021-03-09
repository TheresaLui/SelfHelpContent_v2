<properties
	pageTitle="Azure Load Balancer Connectivity Issues - Cannot connet to a specific port"
	description="Azure Load Balancer Connectivity Issues - Cannot connect to a specific port"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781318"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6e"
	ownershipId="CloudNet_LoadBalancer"
/>

# No inbound connectivity to a specific port

## **Recommended Steps**

* A [load balancing rule](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard#create-a-load-balancer-rule) or [inbound NAT rule](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal) is required to establish an inbound connection. Make sure the rules are created.
* You can [combine data path availability and health probe status metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-diagnose-my-load-balancer-deployment) to identify where to look for the problem and how to resolve it.
* Load-balanced endpoints may not respond if all the VMs in the backend pool are detected as unhealthy through health probes. Follow [these instructions](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#are-the-backend-instances-for-my-load-balancer-responding-to-probes) to check whether the backend instances for your load balancer are responding to probes.
* Use the following steps after ensuring backend instances are responding to the probes:
  - No network security group is blocking connectivity to the load balanced service from the expected clients and Azure load balancer probe IP 168.63.129.16. You can use the [Connection Troubleshoot](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-portal?WT.mc_id=Portal-Microsoft_Azure_Support#check-remote-endpoint-connectivity) feature on Network Watcher for this step.
  - No OS level firewall or security software is blocking connectivity to the service from the expected clients and Azure load balancer probe IP 168.63.129.16
  - The service is running and listening on the port configured for the endpoint and the load balancer monitoring probe
