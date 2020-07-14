<properties
	pageTitle="I can't register the device to the service"
	description="I can't register the device to the service"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="8000Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="dff218c2-0aca-4923-86c4-96303d69342e"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# I can't register the device to the service.

If your registration fails, this may be due to one of the following reasons:

## **Recommended steps**

* Your registration key may be incorrect.
 * Verify that you are using the registration key for the StorSimple Device Manager for Physical Series.
 * To get the service registration key, go to your StorSimple Device Manager blade and then go to **Management** > **Keys**. For detailed instructions, go to [Get a service registration key](https://aka.ms/ss8000-ts-regenkey).
* Your device time may be out of sync.
 * In the Windows PowerShell interface of your device, run the *Set-HcsSystem -Timezone* command. Adjust the time zone. Ensure that the time zone input is in the appropriate case. Each initial letter needs to be capitalized, for instance, "Pacific Standard Time".
 * Use the *Sync-HcsTime* cmdlet to display device time and force a time sync with the NTP server. For more information, go to [Troubleshoot with Sync-HcsTime cmdlet](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-sync-hcstime-cmdlet).
* Your proxy server settings may be incorrect. Ensure that you use a valid proxy server while registering. For more information, go to [Configure web proxy for your StorSimple device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-configure-web-proxy).
* Ensure that firewall is configured to meet the [Networking requirements for your StorSimple device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-requirements-for-your-storsimple-device)
* If this is not the first device that you are registering with this service, verify that the service data encryption key is correct. This key is obtained when you registered the first physical device with your StorSimple Device Manager service.

## **Recommended documents**

[Troubleshoot errors during device registration](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#errors-during-device-registration)<br>
[Use Windows PowerShell for StorSimple to administer your device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-windows-powershell-administration)<br>
[Get a service registration key](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-service#get-the-service-registration-key)<br>
[Networking requirements for your StorSimple device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-requirements-for-your-storsimple-device)
