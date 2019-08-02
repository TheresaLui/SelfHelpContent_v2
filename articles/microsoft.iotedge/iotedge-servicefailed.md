<properties
	pageTitle="The iotedged service is in a failed state"
	description="The iotedged service is in a failed state"
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

# The iotedged service is in a failed state

If the IoT Edge service is reporting a failed state, there are several possible causes, including an error in the connection string, firewall connection errors, the container engine not running, or more. IoT Edge has a built-in troubleshooting tool that was developed to check all these common errors for you at once. 

## **Recommended steps**

Run the IoT Edge troubleshooting tool on your IoT Edge device.

* On Linux devices: `sudo iotedge check --verbose`
* On Windows devices: `iotedge check --verbose`

## **Recommended documents**

[Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)<br>
[Built-in troubleshooting functionality](https://github.com/Azure/iotedge/blob/master/doc/troubleshoot-checks.md)