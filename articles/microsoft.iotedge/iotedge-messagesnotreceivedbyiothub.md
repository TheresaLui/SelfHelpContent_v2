<properties
	pageTitle="Device-to-cloud messages aren't reaching IoT Hub"
	description="Device-to-cloud messages aren't reaching IoT Hub"
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

# Device-to-cloud messages aren't reaching IoT Hub

If you aren't seeing messages arriving at IoT Hub from your IoT Edge device, trace the message path from the original module to see which step in the communication pipeline is failing. 

## **Recommended steps**

* Run the troubleshooting tool on your IoT Edge device to check that the device can connect to IoT Hub.
  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`
* Double check the routes in the deployment manifest to verify that all module inputs and outputs are identified correctly.
* Inspect module logs and the IoT Edge hub logs to look for errors or message received confirmations. Use the command `iotedge logs {module name}`.
* Check whether you've reached the IoT Hub quota limits or if your messages are being throttled. The IoT Edge hub should report 429 or 408 errors in those cases. 

## **Recommended documents**

[Azure IoT Edge standard diagnostic steps](https://docs.microsoft.com/azure/iot-edge/troubleshoot#standard-diagnostic-steps)<br>
[IoT Hub quotas and throttling](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)