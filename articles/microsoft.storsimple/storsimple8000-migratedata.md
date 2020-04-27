<properties
	pageTitle="How can I move data from one device to another device"
	description="How can I move data from one device to another device"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="8000Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1399981a-f4fc-4c35-a7d7-ddf2000c58ca"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# How can I move data from one device to another device

When migrating the data from one StorSimple device to another device, consider the following information:

## **Recommended steps**

* If migrating data from 5000-7000 series to a StorSimple 8000 series device, for detailed instructions, go to [Microsoft Azure StorSimple 8000 Series Migration Guide](https://gallery.technet.microsoft.com/Azure-StorSimple-50007000-c1a0460b).
* If you're migrating from other storage device, go to [Migrating data to Storsimple Guide](http://download.microsoft.com/download/9/4/A/94AB8165-CCC4-430B-801B-9FD40C8DA340/Migrating%20Data%20to%20StorSimple%20Volumes_09-02-15.pdf)
* If using device failover to change the data ownership, be aware that:
 * Failover is not supported if the two devices are registered to different StorSimple Device Managers.
 * Failover is only possible when the two devices are registered to the same StorSimple Device Manager service.

## **Recommended documents**

[Failover and disaster recovery for StorSimple 8000 series devices](https://docs.microsoft.com/azure/storsimple/storsimple-8000-device-failover-disaster-recovery)