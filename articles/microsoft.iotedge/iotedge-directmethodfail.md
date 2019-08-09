<properties
	pageTitle="Direct method execution fails"
	description="Direct method execution fails"
	service="microsoft.devices"
	resource="iotedge"
	authors="kgremban"
	ms.author="kgremban"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="5848a8ba-3d79-4c83-8e01-5042226bc87f"
/>

# Direct method execution fails

Direct method calls to IoT Edge modules require an open connection. When troubleshooting direct method failures, start by verifying that the module can be reached. 

## **Recommended steps**

* Run the troubleshooting tool on your IoT Edge device to check that the device can connect to IoT Hub.
  
  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`

* If your IoT Edge device is not running the latest version, upgrade to version 1.0.7-1 or newer to take advantage of an SDK fix for intermittent connectivity issues.

## **Recommended documents**

[Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)<br>
[Update the IoT Edge security daemon and runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge)