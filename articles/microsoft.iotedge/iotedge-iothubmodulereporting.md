<properties
	pageTitle="The Azure portal doesn't report IoT Edge modules as running"
	description="The Azure portal doesn't report IoT Edge modules as running"
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

# The Azure portal doesn't report IoT Edge modules as running

There are several ways to check whether a module is running on your IoT Edge device. If the status reported in the Azure portal doesn't seem correct, use these other methods to inspect your module.

## **Recommended steps**

* Use the [Azure IoT Tools for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=vsciot-vscode.azure-iot-tools) or the [Azure IoT Edge tools for Visual Studio 2019](https://marketplace.visualstudio.com/items?itemName=vsc-iot.vs16iotedgetools) extensions to monitor and manage your IoT Edge devices and modules. 
* Use a direct method to ping the IoT Edge agent or the module and get its status.
* On the IoT Edge device, use the command `iotedge list` to check the status of all modules on the device. If your module is not running, use the command `iotedge logs <module name>` to get more information.
* For ongoing reporting, consider using Event Grid to monitor connect and disconnect events. 

## **Recommended documents**

[Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)<br>
[React to IoT Hub events by using Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)