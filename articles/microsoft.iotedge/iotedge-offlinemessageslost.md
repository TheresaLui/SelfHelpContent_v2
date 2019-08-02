<properties
	pageTitle="Messages are lost or my device runs out of resources after going offline"
	description="Messages are lost or my device runs out of resources after going offline"
	service="microsoft.devices"
	resource="iotedge"
	authors="kgremban"
	ms.author="kgremban"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# Messages are lost or my device runs out of resources after going offline

Azure IoT Edge is designed to operate while offline, and then forward stored messages after regaining connection. If your IoT Edge device loses messages or runs out of resources, check to make sure that your device is configured with the store-and-forward settings that fit your solution.

## **Recommended steps**

* Review the [Optional offline settings](https://docs.microsoft.com/azure/iot-edge/offline-capabilities#optional-offline-settings) and adjust the time to live settings and offline storage capabilities to suit your scenario.
* If your IoT Edge device is small, review the troubleshooting steps for [Stability issues on resource constrained devices](https://docs.microsoft.com/azure/iot-edge/troubleshoot#stability-issues-on-resource-constrained-devices)

