<properties
	pageTitle="My problem relates to an IoT Edge module"
	description="My problem relates to an IoT Edge module"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680936,32680937,32680940,32680944,32680947,32680948,32680954,32680964,32680968,32680984"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="6f19909d-9bcc-44f5-be02-e7777aba61ee"
	ownershipId="AzureIot_IotEdge"
/>

# My problem relates to an IoT Edge module

Whether deploying custom code or an Azure service as an IoT Edge module, there are some common errors that you can check.

## **Recommended Steps**

* Use the built-in troubleshooting tool to check for common configuration or connection errors:

  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`

* Restart the module: `iotedge restart <module name>`
* Remove the module from the device and have the IoT Edge agent pull the module image again:

  * On Linux devices: `sudo docker ps -a` to get the container names, then `sudo docker rm -f <container name>`
  * On Windows devices: `docker -H npipe:////./pipe/iotedge_moby_engine ps -a` to get the container names, then `docker -H npipe:////./pipe/iotedge_moby_engine rm -f <container name>`

* If your module is a third-party module from the [IoT Edge module marketplace](https://azuremarketplace.microsoft.com/marketplace/apps/category/internet-of-things?page=1&subcategories=iot-edge-modules), refer to their documentation for additional information

## **Recommended Documents**

* [Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)
* [Container management for production deployments](https://docs.microsoft.com/azure/iot-edge/production-checklist#container-management)
