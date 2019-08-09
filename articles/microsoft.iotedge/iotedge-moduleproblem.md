<properties
	pageTitle="My problem relates to an IoT Edge module"
	description="My problem relates to an IoT Edge module"
	service="microsoft.devices"
	resource="iotedge"
	authors="kgremban"
	ms.author="kgremban"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="6f19909d-9bcc-44f5-be02-e7777aba61ee"
/>

# My problem relates to an IoT Edge module

Whether deploying custom code or an Azure service as an IoT Edge module, there are some common errors that you can check.

## **Recommended steps**

* Use the built-in troubleshooting tool to check for common configuration or connection errors. 
  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`
* Restart the module: `iotedge restart <module name>`
* Remove the module from the device and have the IoT Edge agent pull the module image again. 
  * On Linux devices: `sudo docker ps -a` to get the container names, then `sudo docker rm -f <container name>`
  * On Windows devices: `docker -H npipe:////./pipe/iotedge_moby_engine ps -a` to get the container names, then `docker -H npipe:////./pipe/iotedge_moby_engine rm -f <container name>`
* If your module is a third-party module from the [IoT Edge module marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/category/internet-of-things?page=1&subcategories=iot-edge-modules), refer to their documentation for additional information. 

## **Recommended documents**

[Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)<br>
[Container management for production deployments](https://docs.microsoft.com/azure/iot-edge/production-checklist#container-management)