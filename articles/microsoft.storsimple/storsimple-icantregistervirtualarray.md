<properties
	pageTitle="I can't register my virtual array"
	description="I can't register my virtual array."
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I can't register my virtual array
If your registration fails, it could be due to one of the following reasons.

## **Recommended steps**
1. Your registration key may be incorrect. Verify your registration key. Go to **Management** > **Keys** to get the service registration key <br>
[Registration key](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade).
2. If this is not the first device that you are registering with this service, verify that the service data encryption key is correct. In the local web UI of any virtual array registered with this service, go to **Configuration** > **Cloud settings** and click **Get service data encryption key**.
3. Your device time may be out of sync. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Modify the NTP server settings if a time offset is reported.
4. Your proxy server settings may be incorrect. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Update the proxy server settings if a discrepancy is reported.


## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[Get the service registration key](https://aka.ms/storsimple-troubleshoot-registerkey)<br>
[StorSimple Virtual Array system requirements](https://aka.ms/storsimple-troubleshoot-va-reqs)
