<properties
	pageTitle="I can't register my virtual array."
	description="I can't register my virtual array."
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="9000Or1200Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8f48e255-7e25-4135-840c-41e11861e7b8"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# I can't register my virtual array.
If your registration fails, do the following.

## **Recommended steps**
1. Your registration key may be incorrect. Verify your registration key. Go to [**Management** > **Keys**](data-blade:Microsoft_Azure_StorSimple.RegistrationKeyBlade) to get the service registration key.
2. If this is not the first device that you are registering with this service, verify that the service data encryption key is correct. In the local web UI of any virtual array registered with this service, go to **Configuration** > **Cloud settings** and click **Get service data encryption key**.
3. Your device time may be out of sync. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Modify the NTP server settings if a time offset is reported.
4. Your proxy server settings may be incorrect. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Update the proxy server settings if a discrepancy is reported.


## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[Get the service registration key](https://aka.ms/storsimple-troubleshoot-registerkey)<br>
[StorSimple Virtual Array system requirements](https://aka.ms/storsimple-troubleshoot-va-reqs)
