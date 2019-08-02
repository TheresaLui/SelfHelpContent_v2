<properties
	pageTitle="The IoT Edge runtime times out when trying to connect to IoT Hub"
	description="The IoT Edge runtime times out when trying to connect to IoT Hub"
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

# The IoT Edge runtime times out when trying to connect to IoT Hub

If your IoT Edge device fails while trying to connect to IoT Hub, use the following steps to inspect the device's connection and configuration. 

## **Recommended steps**

* Run the troubleshooting tool on your IoT Edge device. Pay particular attention to the results of the connectivity checks.
  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`
* If your network uses a proxy for eternal communication, follow the steps to [Configure an IoT Edge device to communicate through a proxy server](https://docs.microsoft.com/azure/iot-edge/how-to-configure-proxy-support).
* If your network is behind a firewall, review the [Firewall and port configuration rules for IoT Edge deployments](https://docs.microsoft.com/azure/iot-edge/troubleshoot#firewall-and-port-configuration-rules-for-iot-edge-deployment)

## **Recommended documents**

[Built-in troubleshooting functionality](https://github.com/Azure/iotedge/blob/master/doc/troubleshoot-checks.md)<br>
[Networking checklist for IoT Edge deployments](https://docs.microsoft.com/azure/iot-edge/production-checklist#networking)