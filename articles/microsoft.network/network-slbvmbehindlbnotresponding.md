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
4.	Remote into a VM behind the LB and run command "netstat -an" (for Windows) <forLinux>.<br>
	If you don't see TCP port listed in the results, you may need to configure the application on the VM to listen and respond on the probe and data ports.<br>
5.	Use [Psping](https://technet.microsoft.com/sysinternals/psping.aspx) for Windows VM <forLinux> within the VNet (not behind the LB) to test the probe and data ports response (example: psping 10.0.0.4:80). If you do not receive responses, check to ensure that a NSG/UDR isn't blocking.<br>
6.	Run a simultaneous network trace on the LB VM and the VNet test VM while you run PsPing <forLinux> then stop the trace <linkstoNetshandTCPdump>.<br>
	a. For Windows, open command prompt on both VMs and run the following: netsh trace start capture=yes tracefile=c:\server_IP.etl scenario=netconnection<br>
	b. Use psping from the Vnet VM to the LB VM (example: psping 10.0.0.4:80)<br>
	c. Open the Netsh trace from the backend VM with Network Monitor and apply a display filter for the IP of the VM you ran PsPing from, such as, "IPv4.address==10.0.0.4"<br>
	If you do not see the packets incoming to the backend VM trace, there is likely a NSG/UDR interfering. If you do see the packets coming in but no response, then you may need to address a VM application or a firewall issue.<br>
7.	Internal Load-Balancer (ILB): If issue only occurs from your on-premises network through VPN/ExpressRoute and doesn't reproduce from a VM within a Vnet, test communication from on-premises resources to another non-load balanced VM in the VNet over the VPN/ExpressRoute.
8.	External Load-Balancer (ELB/SLB): If the issue only occurs from on-premises network to the public IP address of the Load-Balancer and not another location (such as home or coffee shop), it is likely a proxy or firewall setting on-premises.<br>
9.	External Load-Balancer (ELB/SLB): If you have a VPN/ExpressRoute and [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm) or a [Default Route](https://github.com/Azure/azure-content/blob/master/articles/expressroute/expressroute-routing.md) on the Vnet or LB subnet can cause asynchronous routing which will disrupt proper communication routing.

## **Recommended documents**
Log Analytics for Azure Load Balancer [LB diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)<br>
Configure [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)
