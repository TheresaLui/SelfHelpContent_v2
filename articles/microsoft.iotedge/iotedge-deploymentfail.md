<properties
	pageTitle="Deployments aren't getting applied to an IoT Edge device"
	description="Deployments aren't getting applied to an IoT Edge device"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680949"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="f9fb9e78-587e-4766-8573-762030330d71"
	ownershipId="AzureIot_IotEdge"
/>

# Deployments aren't getting applied to an IoT Edge device

IoT Edge deployment manifests describe the modules that should be running on an IoT Edge device, and declares how they should be configured and how they can communicate with each other. If a deployment is applied to an IoT Edge device but the changes don't appear, it's usually because there's a connectivity issue or the deployment manifest isn't formatted correctly. 

## **Recommended Steps**

* Verify that the deployment manifest lists the correct module names, module images, and includes the credentials for any private container registries. 

* If it's an automatic deployment, verify that the tags in the device twin match the target condition for the deployment. And check that another deployment doesn't have higher priority for that device. 

* On the IoT Edge device, run the command **iotedge check --verbose**. Look particularly at the results of the connectivity checks to make sure that your device can connect to IoT Hub to retrieve deployment updates. 

* Run the command **iotedge logs edgeAgent** to check the IoT Edge agent logs for any errors or failures. The agent is responsible for retrieving deployments and starting the modules, so these logs should help identify which part of the process is failing. 

## **Recommended Documents**

* [IoT Edge agent module continually reports 'empty config file' and no modules start on the device](https://docs.microsoft.com/azure/iot-edge/troubleshoot-common-errors#edge-agent-module-reports-empty-config-file-and-no-modules-start-on-the-device)