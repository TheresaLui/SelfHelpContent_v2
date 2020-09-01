<properties
	pageTitle="My device appears offline in the portal"
	description="My device appears offline in the portal"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="8000Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="11fcd55e-e56b-47be-946c-feaf4447b11d"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# My device appears offline in the portal.

If your device is offline, then the device is not able to communicate with the StorSimple Device Manager service. This could be due to one of the following reasons:

## **Recommended steps**

* The Internet connectivity is broken. In the Windows PowerShell interface of your device, run *Test-HcsmConnection*. Resolve the reported issues. For more information, go to  [Troubleshoot with the Test-HcsmConnection cmdlet](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-test-hcsmconnection-cmdlet).
* One or more of your network interfaces has issues. Run the *Get-NetAdapter* cmdlet to verify the health of your network interface. For more information, go to [Troubleshoot with the Get-NetAdapter cmdlet](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-get-netadapter-cmdlet).
* The device is turned off. For more information, go to [Turn on your StorSimple 8000 series device](https://docs.microsoft.com/azure/storsimple/storsimple-turn-device-on-or-off).
* Your web proxy settings are incorrect. For more information, go to [Configure and view the web proxy settings for your device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-configure-web-proxy).
* Your device time may be out of sync with the Internet time. Verify your time zone and NTP server settings. Run the *Sync-HcsTime* to force a device time sync with the NTP server. For detailed instructions, go to [Troubleshoot with Sync-HcsTime cmdlet](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-sync-hcstime-cmdlet).

## **Recommended documents**

[Tools for troubleshooting StorSimple deployments](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#tools-for-troubleshooting-storsimple-deployments)