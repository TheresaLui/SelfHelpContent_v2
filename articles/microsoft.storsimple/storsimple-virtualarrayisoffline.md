<properties
	pageTitle="My virtual array is offline"
	description="My virtual array is offline"
	service="microsoft.storsimple"
	resource="storsimpledevicemanagers"
	authors="anbacker"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# My virtual array is offline
If your virtual array is offline, this could be due to one of the following reasons:
* Your virtual array may be turned off on the hypervisor.
* Your virtual array is not able to communicate with the StorSimple Device Manager service.

## **Recommended steps**
* In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**.
* Your VM could have rebooted due to a windows update. Wait a few minutes and try again to connect.
* If you cannot connect again check from the Hyper-V host or ESX server to ensure that the VM is healthy.


## **Recommended documents**
[Troubleshoot via the local web UI](https://azure.microsoft.com/documentation/articles/storsimple-ova-web-ui-admin/#troubleshoot-web-ui-setup-errors)<br>