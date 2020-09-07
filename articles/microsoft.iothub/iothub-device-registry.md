<properties
	pageTitle="Can't create, update, or delete devices"
	description="Can't create, update, or delete devices"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="generic"
	supportTopicIds="32630542"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="d7aee04b-0898-4166-9bde-b41437508872"
	ownershipId="AzureIot_IotHub"
/>

# Can't create, update, or delete devices

## **Recommended Steps**

1. Review the limits on device identity operations to make sure that you're under them:

* **Create, retrieve, list, update, or delete device identities**: 83.33/sec/unit (5,000/min/unit) for B3 and S3; 1.67/sec/unit (100/min/unit) for all other tiers

* **Device count**: The maximum number of devices you can register to a single IoT hub is 1,000,000. The only way to increase this limit is to contact Microsoft Support.

* **Device import and export jobs**: IoT Hub only allows 1 device import/export job to run at a time

1. If you have [logs turned on](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#cloud-to-device-commands), check for errors under the DeviceIdentitiesOperations category:

* [404001 DeviceNotFound](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-404001-devicenotfound)
* [409001 DeviceAlreadyExists](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-409001-devicealreadyexists)
* [500xxx Internal errors](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-500xxx-internal-errors)

## **Recommended Documents**

* [Understand and manage the device identity registry](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-identity-registry)<br>

