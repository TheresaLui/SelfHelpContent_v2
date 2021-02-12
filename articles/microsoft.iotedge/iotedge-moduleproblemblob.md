<properties
	pageTitle="Problems with the Azure Blob Storage on IoT Edge module"
	description="Problems with the Azure Blob Storage on IoT Edge module"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680941"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="7dac9352-936d-4a83-be0f-8d957dcc3347"
	ownershipId="AzureIot_IotEdge"
/>

# Problems with the Azure Blob Storage on IoT Edge module

The Azure Blob Storage on IoT Edge module enables local storage that can also sync to the cloud. Issues with this module tend to arise from connection errors. 

## **Recommended Steps**

* Make sure that your IoT Edge device, the local storage location, and any apps that may create or query the blob data can connect to each other. If they're on different devices, make sure the appropriate ports are open for sending and receiving messages, or for going through any firewalls or proxies in between. 
* If the issue is with uploading data to blob storage in the cloud, use the built-in troubleshooting tool to make sure that the IoT Edge device is connected to IoT Hub:

	* On Linux devices: `sudo iotedge check --verbose`
  	* On Windows devices: `iotedge check --verbose`

## **Recommended Documents**

* [Store data at the edge with Azure Blob Storage on IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-store-data-blob)
* [Deploy the Azure Blob Storage on IoT Edge module to your device](https://docs.microsoft.com/azure/iot-edge/how-to-deploy-blob)
