<properties
	pageTitle="Check the guest for VM NIC issues"
	description="Check the guest for VM NIC issues"
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
	articleId="66382dd4-1e72-4fc3-8d2a-8252a9c34532"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check the guest for VM NIC issues

1. When you have run NetVMA for the timeframe of the issue, select the VM and then click on the right hand site on "VFP Port Metrics/'Web Dashboard" to check VM network related communication
2. Understand if VSC State is always up (chart: VscState and VspPaused = "3")
3. Check Inbound and Outbound communication for drops to "0" (charts: Inbound Packets, Outbound Packets, Bytes Sent/Received (VFP), Bytes Sent/Received (VMSwitch)
4. Check for interruption in VFP Flows (charts: Inbound VFP Flows, Outbound VFP Flows)
5. Determine VSC state
    1. If you don't see the bytes sent/received counter go to 0, and the VSC state/paused did not go to 0, then that indicates VSC was up all the time and this indicates an issue with the guest OS
    2. If you see VSC state go to 0, then that indicates a host layer communication issue with the VM
