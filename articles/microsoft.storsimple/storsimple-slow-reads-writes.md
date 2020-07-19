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

### StorSimple

- If not already done, enable additional interface(s) for iSCSI traffic to segregate cloud traffic and iSCSI traffic
- Ensure that a dedicated cloud bandwidth of at least 40Mbps is available to StorSimple device

### Network

- [Ensure that cloud IPs (cloud-enabled interfaces and controller fixed IPs on StorSimple) are configured based on ports and URL best practices](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-requirements-for-your-storsimple-device)
- Ensure that cloud bandwidth available to StorSimple is 40Mbps or more and is dedicated to the device in case of shared internet link

## **Recommended Documents**

* [StorSimple 8000 Series Deployment Best Practices](https://gallery.technet.microsoft.com/Azure-StorSimple-8000-72b01b68)<br>

