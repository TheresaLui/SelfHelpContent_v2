<properties
	pageTitle="My issue is not listed"
	description="My issue is not listed"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680977,32680978"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="c2aa9204-a06a-4516-b33f-47a985b17833"
	ownershipId="AzureIot_IotEdge"
/>

# My issue is not listed

If your IoT Edge issue isn't listed in the support options, a good first step is to run the built-in troubleshooting tool on your IoT Edge device. It checks for the most common configuration and connection errors. Even if the troubleshooting tool doesn't flag anything on your device, it's still helpful to eliminate those common errors.

## **Recommended Steps**

Run the IoT Edge troubleshooting tool on your IoT Edge device:

* Linux devices: `sudo iotedge check --verbose`
* Windows devices: `iotedge check --verbose`

If you open a support case, include the output of the troubleshooting tool to help your case manager get to a resolution faster. 

## **Recommended Documents**

* [Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)
* [Built-in troubleshooting functionality](https://github.com/Azure/iotedge/blob/master/doc/troubleshoot-checks.md)
