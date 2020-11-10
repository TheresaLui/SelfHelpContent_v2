<properties
	pageTitle="Read or write to volume/share is slow"
	description="Read or write to volume/share is slow troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="archana-msft"
	ms.author="armukk"
	displayOrder=""
	articleId="dafaf48e-329e-4686-ab0a-3fe0db140a37"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630506"
	resourceTags="8000Series"
	productPesIds="15438"	
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Read or write to volume/share is slow

## **Recommended Steps**

Recommendations for configuring Host, StorSimple, and Network to address performance issues.

### Host

- Antivirus for tiered volumes should be configured to scan on open and close and not full scan
- Disable indexing on directories if it is enabled on StorSimple tiered volumes
- Disable VSS (if enabled on StorSimple volumes) or move the VSS destination to locally pinned vol or an external disk
- Disable defragmentation if enabled on StorSimple volumes
- [Configure MPIO as suggested in the best practices documentation](https://gallery.technet.microsoft.com/Azure-StorSimple-8000-72b01b68)  
- Add interface(s) dedicated only for iSCSI traffic and segregate iSCSI traffic from production traffic using separate vlans
- If local only and tiered volumes are configured on StorSimple device, make sure that both types of volumes are not presented to the same host to avoid any performance issues
- Reformatting a thinly provisioned volume may take a long time. We recommend deleting the volume and then creating a new one instead of reformatting. However, if you still prefer to reformat a volume:
    - Run the following command before the reformat to avoid space reclamation delays: `fsutil behavior set disabledeletenotify 1`
    - After the formatting is complete, use the following command to re-enable space reclamation: `fsutil behavior set disabledeletenotify 0`

### StorSimple

- If not already done, enable additional interface(s) for iSCSI traffic to segregate cloud traffic and iSCSI traffic
- Ensure dedicated bandwidth of 40Mbps is available to the StorSimple device and for enhanced performance ensure that more dedicated bandwidth is available<br>

### Network

- [Ensure that cloud IPs (cloud-enabled interfaces and controller fixed IPs on StorSimple) are configured based on ports and URL best practices](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-requirements-for-your-storsimple-device)
- Ensure that cloud bandwidth available to StorSimple is 40Mbps or more and is dedicated to the device in case of shared internet link

## **Recommended Documents**

* [StorSimple 8000 Series Deployment Best Practices](https://gallery.technet.microsoft.com/Azure-StorSimple-8000-72b01b68)<br>

