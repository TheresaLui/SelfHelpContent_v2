<properties
	pageTitle="My device appears offline in the portal."
	description="My device appears offline in the portal."
	service="Microsoft.DataBoxEdge"
	resource="databoxedgedevices"
	authors="anbacker"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public"
/>

# My device appears offline in the portal

## **Recommended steps**

If your device is offline, this could be due to one of the following reasons:

1. The device is not able to communicate with the Azure service. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve the reported issues.
2. The device may be turned off or paused on the hypervisor.

    * Your device could have rebooted due to a Windows update. Wait a few minutes and try to reconnect.
    * In Hyper-V, your device will be paused automatically when the volume that stores snapshots or virtual hard disks, runs out of available storage. The state of the device is listed as *paused-critical* in Hyper-V Manager. Resolve this by creating additional space on the volume.
    * If you still cannot connect, check the Hyper-V host or ESX server to ensure that the VM is healthy.

3. Your proxy server settings may be incorrect. Ensure that you use a valid proxy server while registering. For more information, go to [Configure web proxy for your device](https://aka.ms/dbe-device-local-mgmt).

## **Recommended documents**

* [Troubleshoot your Azure Data Box Gateway issues](https://docs.microsoft.com/azure/databox-online/data-box-gateway-troubleshoot)
* [Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)
* [Troubleshooting VM failures on ESXi server](https://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1003976)
