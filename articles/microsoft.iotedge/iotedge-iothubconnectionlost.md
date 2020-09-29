<properties
	pageTitle="Loses connection to IoT Hub over time"
	description="Loses connection to IoT Hub over time"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680962"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="a52ed011-0356-41b1-965f-f640bb3b89cf"
	ownershipId="AzureIot_IotEdge"
/>

# Loses connection to IoT Hub over time

If your IoT Edge device was running successfully for a while, then eventually loses its connection to IoT Hub, something in your configuration may be blocking the connection or you may be running an older version of IoT Edge. 

## **Recommended Steps**

* On the IoT Edge device, run the command **iotedge check --verbose**. Look particularly at the results of the connectivity checks. 
* Check the version of IoT Edge on your device by running the command **iotedge --version**. Update your device to version 1.0.7-1 or newer to take advantage of an SDK fix for intermittent connectivity issues.

## **Recommended Documents**

* [Built-in troubleshooting functionality](https://github.com/Azure/iotedge/blob/master/doc/troubleshoot-checks.md)
* [Detect and troubleshoot disconnects with Azure IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-connectivity)
* [Update the IoT Edge security daemon and runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge)