<properties
	pageTitle="IoT Edge module not connecting"
	description="IoT Edge module not connecting"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680961"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="642e98fe-b62c-4c7e-9550-87f54fab3a9b"
	ownershipId="AzureIot_IotEdge"
/>

# IoT Edge module loses connection

If your IoT Edge device has been running for a while and then modules stop being able to connect, it's probably because something changed in the device's configuration or connection. 

## **Recommended Steps**

* On the IoT Edge device, run the command `iotedge check --verbose`. Look particularly at the results of the configuration checks. If you don't provide certificates during installation, IoT Edge uses preview certificates that expire after 30 days. Reboot the device or use a production certificate to continue using the device. 
* Check the version of IoT Edge on your device by running the command `iotedge --version`. Update your device to version 1.0.7-1 or newer to take advantage of an SDK fix for intermittent connectivity issues.
* Update the IoT Edge agent and IoT Edge hub modules to tag 1.0.8 or newer. For more information, 
	* _1.1 (and earlier)_ See [Update a specific tag image](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2018-06#update-a-specific-tag-image).
	* _1.2 (and later)_ See [Update a specific tag image](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2020-11#update-a-specific-tag-image).

## **Recommended Documents**

**1.1 (and earlier)**

* [Install production certificates](https://docs.microsoft.com/azure/iot-edge/production-checklist?view=iotedge-2018-06#install-production-certificates)
* [How to Update IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2018-06)

**1.2 (and later)**

* [Install production certificates](https://docs.microsoft.com/azure/iot-edge/production-checklist?view=iotedge-2020-11#install-production-certificates)
* [How to Update IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2020-11)

