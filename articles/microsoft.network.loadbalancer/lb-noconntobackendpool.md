<properties
	pageTitle="Azure Load Balancer backend pool connection issues"
	description="Azure Load Balancer backend pool connection issues"
	service="microsoft.network"
	resource="loadbalancers"
	authors="anavinahar"
	ms.author="anavin"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781319"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6b"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer backend pool connection issues

## **Recommended Steps**

* Load Balanced endpoints may not respond if all the VMs in the backend pool are detected as unhealthy via health probes. Learn about [Azure Load Balancer Health probes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview)
* Standard Load Balancer has an extensive set of metrics is available to check the health and status of Load Balancer resource. Please check the [Load Balancer metrics and Diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics) to learn about the common troubleshooting guidance.<br>
* Basic Load Balancer has [Azure Monitor logs](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log) to help determine the root cause
* You can follow [troubleshooting steps](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot) to ensure that:<br>

	- No network security group is blocking connectivity to the load balanced service from the expected clients and Azure load balancer probe IP 168.63.129.16
	- No OS level firewall or security software is blocking connectivity to the service from the expected clients and Azure load balancer probe IP 168.63.129.16
	- The service is running and listening on the port configured for the endpoint and the load balancer monitoring probe
