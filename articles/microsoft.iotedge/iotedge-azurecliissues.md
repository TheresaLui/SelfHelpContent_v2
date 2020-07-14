<properties
	pageTitle="Problems related to the Azure CLI"
	description="Problems related to the Azure CLI"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680938"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="14bc5cb4-01f0-49fb-8757-fc31add23ffc"
	ownershipId="AzureIot_IotEdge"
/>

# Problems related to the Azure CLI

If you encounter errors when running **az iot edge** commands with the Azure CLI, make sure that you're using the latest versions of the Azure CLI and the Azure IoT extension for the CLI. 

## **Recommended Steps**

1. Check your version of the CLI and the IoT extension with the following command: `az --version`

2. [Install the latest version of the Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest)

3. Update the Azure IoT extension with the following command: `az extension update --name azure-cli-iot-ext`

