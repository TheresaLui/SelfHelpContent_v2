<properties
	pageTitle="Device appears offline in portal"
	description="Device appears offline in portal"
	infoBubbleText="See detailson the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="e361b40c-a3c4-434a-afe9-6046186ad050"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630504"
	resourceTags="9000Or1200Series"
	productPesIds="16161"
	cloudEnvironments="public"
/>

# Device appears offline in the portal.
If your virtual array is offline, this could be due to one of the following reasons:

## **Recommended steps**

1. The virtual array is not able to communicate with the StorSimple Device Manager service. <br>
	a. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve the reported issues.
2. The virtual array may be turned off or paused on the hypervisor. <br>
	a. Your virtual array could have rebooted due to a Windows update. Wait a few minutes and try to reconnect.<br>
	b. In Hyper-V, your virtual array will be paused automatically when the volume that stores snapshots or virtual hard disks, runs out of available storage. The state of the virtual array is listed as *paused-critical* in Hyper-V Manager. Resolve this by creating additional space on the volume. <br>
  c. If you still cannot connect, check the Hyper-V host or ESX server to ensure that the VM is healthy.


## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)
