<properties
	pageTitle="My IoT Edge device doesn't reconnect after coming back online"
	description="My IoT Edge device doesn't reconnect after coming back online"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680983"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="ff4317fd-3c49-446d-882b-bef72440ed17"
	ownershipId="AzureIot_IotEdge"
/>

# My IoT Edge device doesn't reconnect after coming back online

Azure IoT Edge is designed to operate while offline, and then automatically reconnect to IoT Hub once online. If your IoT Edge device doesn't reconnect, follow these steps to resolve the problem.

## **Recommended Steps**

* Give the device sufficient time to reconnect. On some platforms, it may take up to 10 minutes. 
* Check the version of IoT Edge on your device by running the command **iotedge --version**. Update your device to version 1.0.7-1 or newer to take advantage of an SDK fix for intermittent connectivity issues.
* Use the built-in troubleshooting tool on the IoT Edge device to check for common connection errors:

	* On Linux devices: `sudo iotedge check --verbose`
  	* On Windows devices: `iotedge check --verbose`

## **Recommended Documents**

* [Update the IoT Edge security daemon and runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge)
