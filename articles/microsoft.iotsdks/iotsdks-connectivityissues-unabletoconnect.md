<properties
	pageTitle="Unable to connect issues"
	description="Unable to connect issues"
	service="microsoft.devices"
	resource="IoTSDKs"
	authors="anusapan"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596726"
	resourceTags=""
	productPesIds="16122"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="f5cfdd96-9dee-4423-a67b-4f2c77369536"
	ownershipId="AzureIot_IotHub"
/>

# Unable to connect issues

## **Recommended steps**

1. Validate IoTHub is available
   * Use latest [DeviceExplorer](https://github.com/Azure/azure-iot-sdk-csharp/tree/master/tools/DeviceExplorer)<br>
   * Enter IoTHub connection string in Device Explorer<br>
   * List devices <br>
     Note: If you are unable to get the list of devices , then, one of the following could be the issue :<br>
     - AMQP Ports could be blocked.<br>
	 - IoTHub could be down. Check for outages [here](https://azure.microsoft.com/status/)<br>
   * Run diagnostics (need NPM capability) <br>
     [https://github.com/Azure/iothub-diagnostics](https://github.com/Azure/iothub-diagnostics)<br>

For more information on IoT monitoring, you can refer the following documents:<br>
[https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c)<br>
[https://docs.microsoft.com/azure/iot-hub/iot-hub-operations-monitoring](https://docs.microsoft.com/azure/iot-hub/iot-hub-operations-monitoring)

## **Recommended documents**
[Use the device SDK for connecting to IoT Hub](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution)<br>
[Reliability features in the device SDK](https://docs.microsoft.com/azure/iot-hub/iot-hub-reliability-features-in-sdks)<br>
