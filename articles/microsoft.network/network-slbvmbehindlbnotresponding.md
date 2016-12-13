<properties
	pageTitle="VMs behind Load Balancer (LB) not responding to requests"
	description="VMs behind Load Balancer (LB) not responding to requests"
	service="microsoft.network"
	resource="loadbalancers"
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
3.	Check the LB Health Probe settings in the portal. If it is configured for HTTP change, it to TCP, test and record results.
4.	Remote into a VM behind the LB and run command "netstat -an" (Windows) or "netstat -an | grep -i listen" (Linux).<br>
	If you don't see the probe and data TCP port listed in the results, you may need to configure the application on the VM to listen and respond on the probe and data ports.
5.	Use [Psping](https://technet.microsoft.com/sysinternals/psping.aspx) for Windows or nmap for Linux within the VNet (not behind the LB) to test the probe and data ports response (example: psping 10.0.0.4:80 or nmap -p 80 10.0.0.4). If you do not receive responses, check to ensure that a NSG/UDR isn't blocking.
6.	Run a simultaneous network trace on the LB VM and the VNet test VM while you run PsPing or nmap then stop the trace.<br>
	a. For Windows, run: "netsh trace start capture=yes tracefile=c:\server_IP.etl scenario=netconnection" or for Linux, run: "sudo tcpdump -s0 -i eth0 -X -w vmtrace.cap" <br>
	b. Use psping or nmap from the Vnet VM to the LB VM (example: psping 10.0.0.4:80 or nmap -p 80 10.0.0.4)<br>
	c. Open the network trace from the backend VM with Network Monitor (Windows) or tcpdump (Linux) and apply a display filter for the IP of the VM you ran PsPing or nmap from, such as "IPv4.address==10.0.0.4" (Windows netmon) or "tcpdump -nn -r vmtrace.cap src or dst host 10.0.0.4" (Linux)<br>
	If you do not see the packets incoming to the backend VM trace, there is likely a NSG/ UDR interfering. If you do see the packets coming in but no response, then you may need to address a VM application or a firewall issue.<br>
7.	Internal Load-Balancer (ILB): If the issue only occurs from your on-premises network through VPN/ ExpressRoute and doesn't reproduce from a VM within a Vnet, test communication from on-premises resources to another non-load balanced VM in the VNet over the VPN/ ExpressRoute. The issue may be related to your VPN/ ExpressRoute connection which should be checked.
8.	External Load-Balancer (ELB/SLB): If the issue only occurs from your on-premises network to the public IP address of the Load-Balancer and not from another location, such as home or coffee shop, it is likely a proxy or firewall setting on-premises.
9.	External Load-Balancer (ELB/SLB): If you have a VPN/ ExpressRoute and [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm) or a [Default Route](https://github.com/Microsoft/azure-docs/blob/master/articles/expressroute/expressroute-routing.md#advertising-default-routes) is applied on the Vnet or LB subnet, this can disrupt proper communication routing.

## **Recommended documents**
Log Analytics for Azure Load Balancer [LB diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)<br>
Configure [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)
