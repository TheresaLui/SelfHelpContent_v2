<properties
	pageTitle="A proxy or firewall is blocking my IoT Edge device's connection to IoT Hub"
	description="A proxy or firewall is blocking my IoT Edge device's connection to IoT Hub"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680945,32680953"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="1671c60b-06e2-4893-9ae7-ac72c78a4994"
	ownershipId="AzureIot_IotEdge"
/>

# A proxy or firewall is blocking my IoT Edge device's connection to IoT Hub

IoT Edge devices need outbound ports to communicate with IoT Hub. If you have a proxy or firewall on your network, that could impact the device's connection to the cloud. 

## **Recommended Steps**

Run the IoT Edge troubleshooting tool on your IoT Edge device to identify common connection errors:

* On Linux devices: `sudo iotedge check --verbose`
* On Windows devices: `iotedge check --verbose`

## **Recommended Documents**

* [Firewall and port configuration rules for IoT Edge deployments](https://docs.microsoft.com/azure/iot-edge/troubleshoot#check-your-firewall-and-port-configuration-rules)
* [Configure an IoT Edge device to communicate through a proxy server](https://docs.microsoft.com/azure/iot-edge/how-to-configure-proxy-support)
* [Networking checklist for IoT Edge deployments](https://docs.microsoft.com/azure/iot-edge/production-checklist#networking)
