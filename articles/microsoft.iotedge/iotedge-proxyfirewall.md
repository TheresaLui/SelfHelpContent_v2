<properties
	pageTitle="A proxy or firewall is blocking my IoT Edge device's connection to IoT Hub"
	description="A proxy or firewall is blocking my IoT Edge device's connection to IoT Hub"
	service="microsoft.devices"
	resource="iotedge"
	authors="kgremban"
	ms.author="kgremban"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="1671c60b-06e2-4893-9ae7-ac72c78a4994"
/>

# A proxy or firewall is blocking my IoT Edge device's connection to IoT Hub

IoT Edge devices need outbound ports to communicate with IoT Hub. If you have a proxy or firewall on your network, that could impact the device's connection to the cloud. 

## **Recommended steps**

Run the IoT Edge troubleshooting tool on your IoT Edge device to identify common connection errors.

* On Linux devices: `sudo iotedge check --verbose`
* On Windows devices: `iotedge check --verbose`

## **Recommended documents**

[Firewall and port configuration rules for IoT Edge deployments](https://docs.microsoft.com/azure/iot-edge/troubleshoot#firewall-and-port-configuration-rules-for-iot-edge-deployment)<br>
[Configure an IoT Edge device to communicate through a proxy server](https://docs.microsoft.com/azure/iot-edge/how-to-configure-proxy-support)<br>
[Networking checklist for IoT Edge deployments](https://docs.microsoft.com/azure/iot-edge/production-checklist#networking)