<properties
	pageTitle="Unable to contact a device from IoT Hub "
	description="Unable to contact a device from IoT Hub"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596669"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# Unable to contact a device from IoT Hub

## **Recommended steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId).

1. Check IoT Hub's C2D error logs for more information. <br>
[IoT Hub diagnostic logs](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#cloud-to-device-commands)<br>

1. See if running connection diagnostics on the device reveal anything. <br>
[IoT Hub connection diagnostics tool](https://github.com/Azure/iothub-diagnostics)<br>

## **Recommended documents**
[Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health)<br>
[Send cloud-to-device messages from IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-c2d)<br>
[Requesting Public IP Address of the IoTHub (nslookup <IoTHubName>.azure-devices.net)](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)
