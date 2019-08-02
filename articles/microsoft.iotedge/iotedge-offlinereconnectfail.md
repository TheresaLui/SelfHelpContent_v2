<properties
	pageTitle="My IoT Edge device doesn't reconnect after coming back online"
	description="My IoT Edge device doesn't reconnect after coming back online"
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

# My IoT Edge device doesn't reconnect after coming back online

Azure IoT Edge is designed to operate while offline, and then automatically reconnect to IoT Hub once online. If your IoT Edge device doesn't reconnect, follow these steps to resolve the problem.

## **Recommended steps**

* Give the device sufficient time to reconnect. On some platforms, it may take up to 10 minutes. 
* Check the version of IoT Edge on your device by running `iotedge --version`. Update your device to version 1.0.7-1 or newer to take advantage of an SDK fix for intermittent connectivity issues.
* Use the built-in troubleshooting tool on the IoT Edge device to check for common connection errors. 
  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`

## **Recommended documents**

[Update the IoT Edge security daemon and runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge)