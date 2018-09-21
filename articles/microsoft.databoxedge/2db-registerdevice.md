<properties
	pageTitle="I can't register the device to the service"
	description="I can't register the device to the service"
	service="microsoft.databoxedge"
	resource="databoxedgedevices"
	authors="anbacker"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="DataBoxEdge,DataBoxGateway"
	productPesIds=""
	cloudEnvironments="public"
/>

# I can't register the device to the service.
If your registration fails, this may be due to one of the following reasons:

## **Recommended steps**
* Your activation key may be incorrect.
 * Verify that you are using the activation key for the respective solutions.
 * To get the activation key, go to your **Overview** blade in the Azure portal.
* Your device time may be out of sync. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve the reported issues.
* Your proxy server settings may be incorrect. Ensure that you use a valid proxy server while registering. For more information, go to [Configure web proxy for your device](https://aka.ms/dbe-device-local-mgmt).
* Ensure that firewall is configured to meet the [Networking requirements for your device](https://aka.ms/dbe-network-req)
