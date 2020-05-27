<properties
	pageTitle="I can't activate my device"
	description="I can't activate my device"
	service="microsoft.databoxedge"
	resource="databoxedgedevices"
	authors="anoobbacker"
	ms.author="anbacker"
	authoralias="anbacker"
	displayOrder="20"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxEdge"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="eb21c147-ac6d-4ffd-bf59-2270722cbf21"
	ownershipId="StorageMediaEdge_DataBox"
/>

# I can't activate my device

## **Recommended Steps**

If your activation fails, this may be due to one of the following reasons:

* Your activation key may be incorrect. Verify that you are using the appropriate activation key for the respective solutions. A Data Box Edge device only works with an activation key corresponding to a Data Box Edge resource. The same is true for Data Box Gateway. To get the activation key, go to **Overview** for your Data Box Edge resource in the Azure portal
* Your device time may be out of sync. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve any reported issues.
* Your proxy server settings may be incorrect. Ensure that you use a valid proxy server while registering. For more information, go to [Configure web proxy for your device](https://docs.microsoft.com/azure/databox-online/data-box-edge-deploy-connect-setup-activate#set-up-and-activate-the-physical-device).
* Ensure that firewall is configured to meet the [Networking requirements for your device](https://docs.microsoft.com/azure/databox-online/data-box-edge-system-requirements#networking-port-requirements)

## **Recommended Documents**

* [Troubleshoot your Azure Data Box Edge issues](https://docs.microsoft.com/azure/databox-online/data-box-edge-troubleshoot)