<properties
	pageTitle="Unable to Access Volumes"
	description="Unable to Access Volumes"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="b29a543b-3746-4950-a71a-b962fcc1a81f"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630508"
	resourceTags="8000Series"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Unable to Access Volumes 

## **Recommended Steps**

1. Verify if the device is online and the volumes are showing online in the portal
2. Check on the file server if the target (StorSimple appliance) is showing as connected. If not, try to establish connection. 
3. If the volumes are visible on the file server but not accessible by any users, try to offline/online the volume
4. If the volumes do not appear on the file server, try to rescan the disk
5. [Run network diagnostics to check if the configured interfaces are enabled, and the Storage account credentials and SSL certificate is valid](https://docs.microsoft.com/azure/storsimple/storsimple-8000-diagnostics#to-run-the-diagnostics-tool)
