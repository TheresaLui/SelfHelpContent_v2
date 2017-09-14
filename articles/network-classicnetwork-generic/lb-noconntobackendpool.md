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
Load balanced endpoints may not respond because all VMs configured to be load balanced have been detected as down by the load balancer. It is recommended that customers [enable load balancer logs](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log) to help determine the root cause.<br>
 
See [troubleshooting documentation](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot) for troubleshooting steps.<br>

This will help you ensure:<br> 
No network security group is blocking connectivity to the load balanced service from the expected clients and Azure load balancer probe IP 168.63.129.16.<br>
No OS level firewall or security software is blocking connectivity to the service from the expected clients and Azure load balancer probe IP 168.63.129.16.<br>
The service is running and listening on the port configured for the endpoint and the load balancer monitoring probe.<br>
