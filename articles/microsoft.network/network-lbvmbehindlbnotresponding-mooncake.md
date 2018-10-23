<properties
    pageTitle="VMs behind Load Balancer (LB) not responding to requests"
    description="VMs behind Load Balancer (LB) not responding to requests"
    service="microsoft.network"
    resource="loadbalancers"
    authors="radwiv"
    displayOrder="15"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
/>

# VMs behind Load Balancer (LB) not responding to requests

## **Recommended steps**

1. For troubleshooting and configuration of the 3rd party network appliances contact the appliance vendor.
2. Enable LB diagnostics for external LBs to determine if the Azure platform is detecting issues.
3. Check if the Virtual Machines in the Load Balancer's Backend Pool are responding to Load Balancer Probe<br>

    1. Check if the Virtual Machines are up and available.<br>
    2. Check if the Virtual Machines are listening on the probe port (use command "netstat -an" (Windows) or "netstat -l" (Linux)).<br>
    3. Check if the Network Security Groups on load balancer backend pool VM allow traffic on probe port (see [Troubleshoot Network Security Groups](https://docs.azure.cn/virtual-network/virtual-network-nsg-troubleshoot-portal))<br>
    4. Check if the effective User Defined Routes are interfering with probe packet routing (see [Troubleshoot Routes](https://docs.azure.cn/virtual-network/virtual-network-routes-troubleshoot-portal))<br>
    5. If the Load Balancer Health Probe is configured for HTTP,  change it to TCP, and validate if it starts responding to probes.<br>

4. Check if the Virtual Machines in the Load Balancer's Backend Pool are receiving and responding to traffic on data port<br>

    1. Check if the Virtual Machines are listening on the data port (use command "netstat -an" (Windows) or "netstat -l" (Linux)).<br>
    2. Check if the Network Security Group on load balancer's backend pool VM allow traffic on data port (see [Troubleshoot Network Security Groups](https://docs.azure.cn/virtual-network/virtual-network-nsg-troubleshoot-portal))<br>
    3. Check if the effective User Defined Routes are interfering with data packet routing (see [Troubleshoot Routes](https://docs.azure.cn/virtual-network/virtual-network-routes-troubleshoot-portal))<br>
    4. Check if a participating VM from backend pool is trying to access the Internal Load Balancer VIP. This is an unsupported scenario.<br>

5. Collect network capture to trace the data packet flow<br>

    1. Run a simultaneous network trace on the Load Balancer VM and another test VM from the same Virtual network (For Windows, run: "netsh trace start capture=yes tracefile=c:\server_IP.etl scenario=netconnection" or for Linux, run: "sudo tcpdump -s0 -i eth0 -X -w vmtrace.cap")<br>
    2. Run a PsPing between the two VMs, and capture some packet exchanges. Stop the trace.<br>
    3. Open the network trace from the backend VM with Network Monitor (Windows) or tcpdump (Linux) and apply a display filter for the IP of the VM you ran PsPing or nmap from, such as "IPv4.address==10.0.0.4" (Windows netmon) or "tcpdump -nn -r vmtrace.cap src or dst host 10.0.0.4" (Linux)<br>
    If you do not see the packets incoming to the backend VM trace, there is likely a NSG/ UDR interfering. If you do see the packets coming in but no response, then you may need to address a VM application or a firewall issue.<br>

6. Connectivity problems from Organization premises over VPN / Express Route<br>

    1. Test connectivity from on-premises network to any non-Load Balanced virtual machine in your virtual network to make sure the VPN/Express Route connection is good.<br>
    2. Test connectivity to Public IP Address from On-premises network as well as outside to make sure On-premises firewall is not blocking the traffic.<br>
    3. Check if you have Forced Tunneling configured, or a Default Route is applied on the Vnet or LB subnet. This can potentially disrupt proper routing.<br>

## **Recommended documents**

* [Troubleshoot Azure Load Balancer](https://docs.azure.cn/load-balancer/load-balancer-troubleshoot)<br>
* Log Analytics for Azure Load Balancer [LB diagnostics](https://docs.azure.cn/load-balancer/load-balancer-monitor-log)<br>
* Configure [Forced Tunneling](https://docs.azure.cn/vpn-gateway/vpn-gateway-forced-tunneling-rm)