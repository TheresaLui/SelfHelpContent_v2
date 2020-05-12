<properties
	pageTitle="The Azure portal doesn't report IoT Edge modules as running"
	description="The Azure portal doesn't report IoT Edge modules as running"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680973"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="0699858c-012b-412b-a7cf-435e22cfbb89"
	ownershipId="AzureIot_IotEdge"
/>

# The Azure portal doesn't report IoT Edge modules as running

There are several ways to check whether a module is running on your IoT Edge device. If the status reported in the Azure portal doesn't seem correct, use these other methods to inspect your module.

## **Recommended Steps**

* Use the [Azure IoT Tools for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=vsciot-vscode.azure-iot-tools) or the [Azure IoT Edge tools for Visual Studio 2019](https://marketplace.visualstudio.com/items?itemName=vsc-iot.vs16iotedgetools) extensions to monitor and manage your IoT Edge devices and modules. 

* Use a direct method to ping the IoT Edge agent and get its status. For example, use the following Azure CLI command: `az iot hub invoke-module-method --method-name "ping" -n <hub name> -d <device name> -m '$edgeAgent'`

* On the IoT Edge device, use the command **iotedge list** to check the status of all modules on the device. If your module is not running, use the command **iotedge logs <module name>** to get more information.

* For ongoing reporting, consider using Event Grid to monitor connect and disconnect events. 

## **Recommended Documents**

* [Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)
* [React to IoT Hub events by using Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)