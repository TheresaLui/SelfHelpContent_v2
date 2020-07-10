<properties
	pageTitle="Check host NIC state"
	description="Check host NIC state"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="63062f31-1013-4134-8a78-031c7ec09804"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check host NIC state

1. Check Compute heartbeat and VSC State in [NetVMA](https://netvma.trafficmanager.net/)
    1. If multiple VMs running on the host a “red” state for Compute heartbeat and VSC at time of the issue it’s worth to investigate deeper from host perspective.
    2. If all other VMs running on the host except the VM with the issue have a “green” state for Compute heartbeat and VSC at time of the issue it’s worth to investigate deeper from guest OS perspective.
2. Understand pingmesh latencies
    1. When you have run NetVMA for the timeframe of the issue, select the node and then click on the right hand site on "Pingmesh Node Latency" to check for high latencies
3. Network related Windows Events
    1. Look at critical/error/warning events for Network provider like mlx4eth63, mlx4_bus, Microsoft-Windows-Hyper-V-VmSwitch in Kusto Table "cluster("vmainsight").database("vmadb").WindowsEventTable" to determine any CloudNet related issues.
4. Hostanalyzer network charts
    1. Look for unusual changes (not a straight line) in these three charts.
       1. Host TCPv4 Connection Active
	   2. Host TCPv5 Connection Failures
	   3. Host Connection Resets
