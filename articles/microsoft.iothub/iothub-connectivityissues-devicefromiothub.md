<properties
	pageTitle="Unable to contact a device from IoT Hub "
	description="Unable to contact a device from IoT Hub"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630539"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="53b04342-1802-47dd-84e1-0d4988baaa01"
/>

# Unable to contact a device from IoT Hub

## **Recommended Steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)
2. Check IoT Hub's C2D error logs for more information: [IoT Hub diagnostic logs](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#cloud-to-device-commands)<br>
3. See if running connection diagnostics on the device reveal anything: [IoT Hub connection diagnostics tool](https://github.com/Azure/iothub-diagnostics)<br>

## **Recommended Documents**
* [Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health)<br>
* [Send cloud-to-device messages from IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-c2d)<br>
* [Requesting Public IP Address of the IoTHub (nslookup <IoTHubName>.azure-devices.net)](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)
