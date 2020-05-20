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
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
	resourceTags="8000Series"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
/>

# Backups are failing or slow 

## **Recommended Steps**

1. [Backups are failing but there are no alerts to indicate that backups have failed. This could happen due to the possibility that the job scheduler is unable to schedule the backup job as the active controller is up and running for a very long time. The issue can be resolved by restarting the active controller](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-device-controller#restart-or-shut-down-a-single-controller)<br>
2. [Run network diagnostics to check if any of the ports are blocked on the firewall, and if so, unblock them](https://docs.microsoft.com/azure/storsimple/storsimple-8000-diagnostics#to-run-the-diagnostics-tool)<br>
3. [Ensure that your StorSimple device has a dedicated 40 Mbps or more bandwidth available at all times](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-best-practices)<br>
4. [What is the snapshot retention limit on per volume basis?](https://docs.microsoft.com/azure/storsimple/storsimple-8000-limits)<br>
5. [It is normal for the first backup of the clone volume to take a few days or weeks to complete as a copy of data is created on the cloud and the time to copy this is determined by the size of the data and Azure latencies](https://docs.microsoft.com/azure/storsimple/storsimple-8000-clone-volume-u2#transient-vs-permanent-clones)