<properties
	pageTitle="VMA RCA"
	description="RCA - Node Service Heal - Node Crash"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Node_Freeze_VMPhu_Long"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public"
/>
# Your resource took a little longer to update

<!--issueDescription-->
We identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This occurrence was caused by an **Azure initiated memory-preserving update action**.
<!--/issueDescription-->

The update process succeeded but your VM was unavailable longer than the expected maximum duration of 30 seconds. RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed during this time. This update is part of routine maintenance on the underlying hosts for this VM.<br> 

During these updates, the VM is frozen for up to 30 seconds and then resumed. Our engineers are alerted to investigate all factors that could have caused your VM to reboot and to apply fixes to affected nodes accordingly.<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability. No action is neeed from you.<br>

## Resources

| To learn about ... | See the following ... |
| --- | ---|
| Maintenance and updates | [Maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/) |
| High availability options (highly recommended) | [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability) |
| Resource health and troubleshooting | [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview) |
<br>


