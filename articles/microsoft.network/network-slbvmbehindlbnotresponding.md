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
4.	Choose a single VM behind the LB to test the following:<br>
	1.	Open a command prompt and run the following to validate there is an application listening on the "probe port" and "data port: netstat -an"<br>
		1.	If the port is not showing listening on either configure the application on the VM to listen and respond on the probe port and data ports.<br><br>
    	2.	Use [Psping](https://technet.microsoft.com/sysinternals/psping.aspx) from a Windows VM within the Vnet (not behind the LB) to test the probe port response (example: psping 10.0.0.4:80) and record results. If you do not receive a response <br>
	  	1.	You may have an NSG/UDR block <br>
	  	2.	Configure the application on the VM to listen and respond on the probe port<br><br>
    	3.	Advanced: Run a simultaneous network trace on the LB VM and the VNet test VM while you run [Psping](https://technet.microsoft.com/sysinternals/psping.aspx) then stop the Netsh trace. <br>
	  	1.	Open cmd prompt on both VMs and run the following command: netsh trace start capture=yes tracefile=c:\server_IP.etl scenario=netconnection<br>
	  	2.	Use psping from the Vnet VM to the LB VM (example: psping 10.0.0.4:80)<br>
	  		1.	Open the Netsh trace from the backend VM with [Network Monitor](https://www.microsoft.com/download/details.aspx?id=4865) and apply a display filter for the IP of the VM you ran PsPing from, such as, "IPv4.address==10.0.0.4"<br>
                	2.	If you do not see the packets incoming to the backend VM trace, there is likely a NSG or UDR interfering<br>
                	3.	If you do see the packets coming in but no response there is an issue with the VM application or firewall that has to be addressed<br>
            	3.	Manually check for a 'Deny All' NSG rule on the NIC of the VM or the subnet that has a higher priority that the default rule that allows LB probes & traffic (NSG must allow LB IP of 168.63.129.16 or LoadBalancer tag)<br>
5.	Internal Load-Balancer (ILB): If issue only occurs from your on-premises network through VPN/ExpressRoute and doesn't reproduce from a VM within a Vnet, test communication from on-premises resources to another non-load balanced VM in the VNet over the VPN
6.	External Load-Balancer (ELB/SLB): If the issue only occurs from on-premises network to the public IP address of the Load-Balancer, try a public IP of a VM in the same Vnet. Also try from home or coffee shop. If it works from other locations the issue lies on-premises. Likely a proxy or firewall setting needs to be addressed.<br>
    	1.	If you have a VPN/ExpressRoute and [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm) or a [Default Route](https://github.com/Azure/azure-content/blob/master/articles/expressroute/expressroute-routing.md) on the Vnet or LB subnet can cause asynchronous routing which will disrupt proper communication routing.

## **Recommended documents**
Log Analytics for Azure Load Balancer [LB diagnostics](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)<br>
Configure [Forced Tunneling](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)
