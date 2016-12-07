<properties
	pageTitle="VMs behind Load Balancer (LB) not responding to requests"
	description="VMs behind Load Balancer (LB) not responding to requests"
	service="microsoft.network"
	resource="loadbalancer"
	authors="radwiv"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# VMs behind Load Balancer (LB) not responding to requests

## **Recommended steps**

1.	For troubleshooting and configuration of the 3rd party network appliances contact the vendor of that appliance.
2.	Enable [LB diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log) for external LBs to determine if the Azure platform is detecting issues.
3.	Check the LB Health Probe settings in the portal. If it is configured for HTTP change it to TCP, test and record results.

5.	Internal Load-Balancer (ILB): If issue only occurs from your on-premises network through VPN/ExpressRoute and doesn't reproduce from a VM within a Vnet, test communication from on-premises resources to another non-load balanced VM in the VNet over the VPN
6.	External Load-Balancer (ELB/SLB): If the issue only occurs from on-premises network to the public IP address of the Load-Balancer, try a public IP of a VM in the same Vnet. Also try from home or coffee shop. If it works from other locations the issue lies on-premises. Likely a proxy or firewall setting needs to be addressed.<br>
    	1.	If you have a VPN/ExpressRoute and [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm) or a [Default Route](https://github.com/Azure/azure-content/blob/master/articles/expressroute/expressroute-routing.md) on the Vnet or LB subnet can cause asynchronous routing which will disrupt proper communication routing.

## **Recommended documents**
Log Analytics for Azure Load Balancer [LB diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)<br>
Configure [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)
