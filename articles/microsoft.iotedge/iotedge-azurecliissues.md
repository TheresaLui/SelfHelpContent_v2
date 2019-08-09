<properties
	pageTitle="Problems related to the Azure CLI"
	description="Problems related to the Azure CLI"
	service="microsoft.devices"
	resource="iotedge"
	authors="kgremban"
	ms.author="kgremban"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="14bc5cb4-01f0-49fb-8757-fc31add23ffc"
/>

# Problems related to the Azure CLI

If you encounter errors when running `az iot edge` commands with the Azure CLI, make sure that you're using the latest versions of the Azure CLI and the Azure IoT extension for the CLI. 

## **Recommended steps**

1. Check your version of the CLI and the IoT extension with the command `az --version`.
1. [Install the latest version of the Azure CLI.](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest)
1. Update the Azure IoT extension with the command `az extension update --name azure-cli-iot-ext`.

