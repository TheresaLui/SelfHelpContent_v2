<properties
	pageTitle="Unable to register the device"
	description="Unable to register the device troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="36a83792-486e-4c87-9853-4409ebbfd371"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630510"
	resourceTags="9000Or1200Series"
	productPesIds="16161"	
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Unable to register the device 

## **Recommended Steps**

1. [Your registration key may be incorrect: please verify your registration key](https://docs.microsoft.com/azure/storsimple/storsimple-virtual-array-deploy1-portal-prep#step-2-get-the-service-registration-key)<br>
2. If this is not the first device that you are registering with this service, verify that the service data encryption key is correct. In the local web UI of any virtual array registered with this service, go to **Configuration** > **Cloud settings** and click **Get service data encryption key**.
3. Your device time may be out of sync. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Modify the NTP server settings if a time offset is reported.
4. Your proxy server settings may be incorrect. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Update the proxy server settings if a discrepancy is reported.


## **Recommended Documents**

* [Troubleshoot via the local web UI](https://docs.microsoft.com/azure/storsimple/storsimple-ova-web-ui-admin#troubleshoot-web-ui-setup-errors)<br>
* [StorSimple Virtual Array system requirements](https://docs.microsoft.com/azure/storsimple/storsimple-ova-system-requirements)
