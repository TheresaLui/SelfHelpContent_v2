<properties
	pageTitle="No connectivity to backend pool"
	description="No connectivity to backend pool"
	service="microsoft.network"
	resource="loadbalancers"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public"
/>

# No connectivity to backend pool
## **Recommended documents**
Load balanced endpoints may not respond if the configure VMs for load balancing are detected as down.<br>
For Load Balancer Standard, an extensive set of metrics is available to check the health and status of Load Balancer resource. Please check the [Load Balancer metrics and Diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics) to learn about the common troubleshooting guidance.<br>

For Load Balancer Basic, it is recommended that customers [enable load balancer logs](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log) to help determine the root cause.<br>

You can follow [troubleshooting steps](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot) to ensure that:<br>
- No network security group is blocking connectivity to the load balanced service from the expected clients and Azure load balancer probe IP 168.63.129.16.<br>
- No OS level firewall or security software is blocking connectivity to the service from the expected clients and Azure load balancer probe IP 168.63.129.16.<br>
- The service is running and listening on the port configured for the endpoint and the load balancer monitoring probe.
