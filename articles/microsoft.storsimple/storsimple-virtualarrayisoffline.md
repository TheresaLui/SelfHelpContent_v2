<properties
	pageTitle="My virtual array is offline"
	description="My virtual array is offline"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# My virtual array is offline
If your virtual array is offline, this could be due to one of the following reasons: <br>
1. Your virtual array may be turned off or got paused on the hypervisor. <br>
2. Your virtual array is not able to communicate with the StorSimple Device Manager service.

## **Recommended steps**
1. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**.
2. Your virtual array could have rebooted due to a Windows update. Wait a few minutes and try again to connect.
3. In Hyper-V, your virtual array will be paused automatically when the volume on which snapshots or virtual hard disks are stored runs out of available storage. The state of the virtual array will be listed as *paused-critical* in Hyper-V Manager. Resolve this by creating additional space on the volume.
4. If you cannot connect again check from the Hyper-V host or ESX server to ensure that the VM is healthy.


## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[Troubleshooting Hyper-V](https://technet.microsoft.com/en-us/library/cc742454.aspx)
