<properties
	pageTitle="My device appears offline in the portal"
	description="My device appears offline in the portal"
	service="microsoft.databoxedge"
	resource="databoxedgedevices"
	authors="anoobbacker"
	ms.author="anbacker"
	authoralias="anbacker"
	displayOrder="60"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="842f687b-c163-4afd-bd6d-914fb4c1d589"
	ownershipId="StorageMediaEdge_DataBox"
/>

# My device appears offline in the portal

## **Recommended Steps**

If your device is offline, it could be due to one of the following:

1. The device is not able to communicate with the Azure service. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve any reported issues.
2. The device may be turned off or paused on the hypervisor:

    * Your device could have rebooted due to a Windows update. Wait a few minutes and try to reconnect.
    * In Hyper-V, your device will be paused automatically when the volume that stores snapshots or virtual hard disks runs out of available storage. The state of the device is listed as *paused-critical* in Hyper-V Manager. Resolve this by creating additional space on the volume.
    * If you still cannot connect, check the Hyper-V host or ESX server to ensure that the VM is healthy.

3. Your proxy server settings may be incorrect. Ensure that you use a valid proxy server while registering. For more information, go to [Configure web proxy for your device](https://docs.microsoft.com/azure/databox-online/data-box-edge-deploy-connect-setup-activate#set-up-and-activate-the-physical-device).

## **Recommended Documents**

* [Troubleshoot your Azure Data Box Gateway issues](https://docs.microsoft.com/azure/databox-online/data-box-gateway-troubleshoot)
* [Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)
* [Troubleshooting VM failures on ESXi server](https://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1003976)
