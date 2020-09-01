<properties
	pageTitle="VMs behind Load Balancer (LB) not responding to requests"
	description="Troubleshoot reasons behind why the load balanced virtual machines are unresponsive"
	service="microsoft.network"
	resource="loadbalancers"
	authors="radwiv"
	ms.author="radwiv"
	category="Connectivity"
	searchTags=""
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="14939f9b-b399-4dd8-a78d-55b79bdd20e8"
	ownershipId="CloudNet_LoadBalancer"
/>

# VMs behind Load Balancer (LB) not responding to requests

## **Recommended Steps**

* For troubleshooting and configuration of the 3rd party network appliances, contact the appliance vendor
* Enable LB diagnostics for external LBs to determine if the Azure platform is detecting issues
* Check if the Virtual Machines in the Load Balancer's Backend Pool are responding to Load Balancer Probe:

	* Check if the Virtual Machines are up and available
	* Check if the Virtual Machines are listening on the probe port (use command `netstat -an` (Windows) or `netstat -l` (Linux))
	* Check if the Network Security Groups on load balancer backend pool VM allow traffic on probe port (see [Troubleshoot Network Security Groups](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal))
	* Check if the effective User Defined Routes are interfering with probe packet routing (see [Troubleshoot Routes](https://docs.microsoft.com/azure/virtual-network/virtual-network-routes-troubleshoot-portal))
	* If the Load Balancer Health Probe is configured for HTTP, change it to TCP, and validate if it starts responding to probes
	
* Check if the Virtual Machines in the Load Balancer's Backend Pool are receiving and responding to traffic on data port:

	* Check if the Virtual Machines are listening on the data port (use command "netstat -an" (Windows) or "netstat -l" (Linux))
	* Check if the Network Security Group on load balancer's backend pool VM allow traffic on data port (see [Troubleshoot Network Security Groups](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal))
	* Check if the effective User Defined Routes are interfering with data packet routing (see [Troubleshoot Routes](https://docs.microsoft.com/azure/virtual-network/virtual-network-routes-troubleshoot-portal))
	* Check if a participating VM from backend pool is trying to access the Internal Load Balancer VIP. This is an unsupported scenario.<br>
	
5. Collect network capture to trace the data packet flow:

	* Run a simultaneous network trace on the Load Balancer VM and another test VM from the same Virtual network (For Windows, run: `netsh trace start capture=yes tracefile=c:\server_IP.etl scenario=netconnection` or for Linux, run: `sudo tcpdump -s0 -i eth0 -X -w vmtrace.cap`)
	* Run a PsPing between the two VMs, and capture some packet exchanges. Stop the trace.<br>
	* Open the network trace from the backend VM with Network Monitor (Windows) or tcpdump (Linux) and apply a display filter for the IP of the VM you ran PsPing or nmap from, such as "IPv4.address==10.0.0.4" (Windows netmon) or "tcpdump -nn -r vmtrace.cap src or dst host 10.0.0.4" (Linux)<br>
	
	If you do not see the packets incoming to the backend VM trace, there is likely a NSG/ UDR interfering. If you do see the packets coming in but no response, then you may need to address a VM application or a firewall issue.<br>
	
* Connectivity problems from Organization premises over VPN / Express Route:

	* Test connectivity from on-premises network to any non-Load Balanced virtual machine in your virtual network to make sure the VPN/Express Route connection is good
	* Test connectivity to Public IP Address from On-premises network as well as outside to make sure On-premises firewall is not blocking the traffic
	* Check if you have Forced Tunneling configured, or a Default Route is applied on the Vnet or LB subnet. This can potentially disrupt proper routing.<br>
	
## **Recommended Documents**

* [Troubleshoot Azure Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot)<br>
* Log Analytics for Azure Load Balancer: [LB diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)<br>
* Configure [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)
