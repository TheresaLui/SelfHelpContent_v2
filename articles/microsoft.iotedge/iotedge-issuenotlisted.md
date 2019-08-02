<properties
	pageTitle="My issue is not listed"
	description="My issue is not listed"
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

# My issue is not listed

If your IoT Edge issue isn't listed in the support options, a good first step is to run the built-in troubleshooting tool on your IoT Edge device. It checks for the most common configuration and connection errors. Even if the troubleshooting tool doesn't flag anything on your device, it's still helpful to eliminate those common errors.

## **Recommended steps**

1. Run the IoT Edge troubleshooting tool on your IoT Edge device.
  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`
2. If you open a support case, include the output of the troubleshooting tool to help your case manager get to a resolution faster. 

## **Recommended documents**

[Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)<br>
[Built-in troubleshooting functionality](https://github.com/Azure/iotedge/blob/master/doc/troubleshoot-checks.md)