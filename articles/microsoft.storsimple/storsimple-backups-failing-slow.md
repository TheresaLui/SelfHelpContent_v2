<properties
	pageTitle="Backups are failing or slow"
	description="Backups are failing or slow troubleshooting"
	infoBubbleText="See detailson the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="3e4019c5-01f6-45f9-8cf0-3ef670ce00c5"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630493"
	resourceTags="8000Series"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Backups are failing or slow 

## **Recommended Steps**

1. [Run network diagnostics to check if any of the ports are blocked on the firewall, and if so, unblock them](https://docs.microsoft.com/azure/storsimple/storsimple-8000-diagnostics#to-run-the-diagnostics-tool)<br>
2. [Ensure that your StorSimple device has a dedicated 40 Mbps or more bandwidth available at all times](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-best-practices)<br>
3. Backups are failing but there are no alerts to indicate that backups have failed. This could happen due to the possibility that the job scheduler is unable to schedule the backup job as the active controller is up and running for a very long time. The issue can be resolved by following below process to perform a controller failover.

### Controller failover procedure

Make sure that all hardware components are shown in healthy status in Azure Portal. If not, please resolve the failure alerts before proceeding with the failover. Perform a controller failover by restarting the active controller by following the below steps.
 
- [Login into the active Controller using PowerShell or serial console](https://docs.microsoft.com/azure/storsimple/storsimple-8000-windows-powershell-administration#connect-remotely-to-storsimple-using-windows-powershell-for-storsimple)<br>
- To restart a controller, at the prompt type: Restart-HcsController. This restarts the controller that you are connected to. When you restart the active controller, it fails over to the passive controller before the restart. Restarting a device is not disruptive to connected initiators, assuming the passive controller is available. If a passive controller is not available or turned off, then restarting the active controller may result in the disruption of service and downtime.
