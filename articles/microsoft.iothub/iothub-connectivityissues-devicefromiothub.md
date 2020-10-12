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
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="53b04342-1802-47dd-84e1-0d4988baaa01"
	ownershipId="AzureIot_IotHub"
/>

# Cloud-to-device messages failing or timing out

## **Recommended Steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)
1. See if running connection diagnostics on the device reveal anything: [IoT Hub connection diagnostics tool](https://github.com/Azure/iothub-diagnostics)
1. If you have [logs turned on](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#cloud-to-device-commands), check for common issues under the category C2DCommands:

- **MessageExpired**: The C2D message expired because the device hasn't processed the message in time. Typically this is because device was offline. To resolve, see [C2D message time to live](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-c2d#message-expiration-time-to-live).

- **DeliveryCountExceeded**: Message was abandoned or the lock timed-out (transition between the Enqueued and Invisible states) too many times, exceeding the configured maxDeliveryCount value. Find the device ID and delivery count values (properties column) and consider [changing the maxDeliveryCount configuration](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-c2d#cloud-to-device-configuration-options).

- [404001 DeviceNotFound](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-404103-devicenotonline)

- [403004 DeviceMaximumQueueDepthExceeded](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-403006-devicemaximumactivefileuploadlimitexceeded)

- [412002 DeviceMessageLockLost](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-412002-devicemessagelocklost)

- [500xxx Internal errors](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-500xxx-internal-errors)

## **Recommended Documents**
* [Turn on logs for cloud-to-device messages](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health)<br>
* [Understand cloud-to-device message life cycle, expiration, and configuration](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-c2d)<br>
* [Requesting Public IP Address of the IoT Hub (nslookup <IoTHubName>.azure-devices.net)](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)
