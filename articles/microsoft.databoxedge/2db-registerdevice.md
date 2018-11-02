<properties
	pageTitle="I can't activate my device."
	description="I can't activate my device."
	service="Microsoft.DataBoxEdge"
	resource="databoxedgedevices"
	authors="anbacker"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxEdge,DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public"
/>

# I can't activate my device

## **Recommended steps**

If your activation fails, this may be due to one of the following reasons:

* Your activation key may be incorrect.
  * Verify that you are using the activation key for the respective solutions. A Data Box Edge device only works with an activation key corresponding to a Data Box Edge resource. The same is true for Data Box Gateway.
  * To get the activation key, go to **Overview** for your Data Box Edge resource in the Azure portal.
* Your device time may be out of sync. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve the reported issues.
* Your proxy server settings may be incorrect. Ensure that you use a valid proxy server while registering. For more information, go to [Configure web proxy for your device](https://aka.ms/dbe-device-local-mgmt).
* Ensure that firewall is configured to meet the [Networking requirements for your device](https://aka.ms/dbe-network-req)

## **Recommended documents**

* [Troubleshoot your Azure Data Box Gateway issues](https://docs.microsoft.com/azure/databox-online/data-box-gateway-troubleshoot)
