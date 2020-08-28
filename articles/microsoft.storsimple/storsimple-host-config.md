<properties
	pageTitle="Host Config"
	description="Host config troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="archana-msft"
	ms.author="armukk"
	displayOrder=""
	articleId="286a518c-fbd6-4d94-bba0-5310bf87da6c"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743013"
	resourceTags="8000Series"
	productPesIds="15438"	
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Host Configuration

## **Recommended Steps**

- Antivirus for tiered volumes should be configured to scan on open and close and not full scan
- Disable indexing on directories if it is enabled on StorSimple tiered volumes
- Disable VSS (if enabled on StorSimple volumes) or move the VSS destination to locally pinned vol or an external disk
- Disable defragmentation if enabled on StorSimple volumes
- [Configure MPIO as suggested in the best practices documentation](https://gallery.technet.microsoft.com/Azure-StorSimple-8000-72b01b68)  
- Add interface(s) dedicated only for iSCSI traffic and segregate iSCSI traffic from production traffic using separate vlans
- Reformatting a thinly provisioned volume may take a long time. We recommend deleting the volume and then creating a new one instead of reformatting. However, if you still prefer to reformat a volume:
    - Run the following command before the reformat to avoid space reclamation delays: `fsutil behavior set disabledeletenotify 1`
    - After the formatting is complete, use the following command to re-enable space reclamation: `fsutil behavior set disabledeletenotify 0`
    
