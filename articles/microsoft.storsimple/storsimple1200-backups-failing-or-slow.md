<properties
	pageTitle="Backups are failing or slow"
	description="Backups are failing or slow troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="ed53eb08-3843-4300-a8e4-7654d404f2d5"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630493"
	resourceTags="9000Or1200Series"
	productPesIds="16161"	
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Backups are failing or are slow 

## **Recommended Steps**

1. [Make sure that the appliance is on the latest software version](https://docs.microsoft.com/azure/storsimple/storsimple-virtual-array-install-update-11)<br>
2. [Ensure that the maximum number of files per share for a file server and maximum number of files per volume for an iSCSI server are as per the recommendations](https://docs.microsoft.com/azure/storsimple/storsimple-ova-limits)<br>
3. [If the backups are failing within a minute of their start time, try moving the backup schedule to a different time](https://docs.microsoft.com/azure/storsimple/storsimple-virtual-array-backup#change-the-backup-start-time)