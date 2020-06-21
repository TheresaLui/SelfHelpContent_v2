<properties
	pageTitle="Issues connecting a device to IoT Hub for the first time"
	description="Issues connecting a device to IoT Hub for the first time"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	ms.author="jlian"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630541"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="1e81a69b-2a16-4764-ba83-337ec03c3809"
	ownershipId="AzureIot_IotHub"
/>

# Issues connecting a device to IoT Hub for the first time

## **Recommended Steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)
2. Try testing the connection with a [default sample](https://docs.microsoft.com/azure/iot-hub/tutorial-connectivity) and running our [diagnostic tool](https://github.com/azure/iothub-diagnostics)
3. If you can get the sample to work, but not your own application, check to see if there's an authorization or firewall issue: [IoT Hub device side troubleshooting guide](https://github.com/Azure/azure-iot-sdk-node/wiki/Troubleshooting-Guide-Devices#cannot-connect-to-your-azure-iot-hub)
4. If you have access to the device either physically or remotely (like SSH), see if you can get the logs from the device to find out more. These logs will also help our support team to help you troubleshoot.
5. Ensure the clock on the device is correct since the [time validity for SAS token is validated on IoT Hub machines](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-security). You may need to sync your device clock with an NTP server.

## **Recommended Documents**

* [Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)<br>
* [Sending Messages to IoT Hubs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c)<br>
* [Monitoring Device Connections in Real-Time with Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)<br>
* [Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)
