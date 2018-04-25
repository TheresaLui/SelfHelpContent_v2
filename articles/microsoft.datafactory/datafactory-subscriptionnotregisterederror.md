<properties 
	pageTitle="Error: The subscription is not registered to use namespace Microsoft.DataFactory" 
	description="I receive the error: The subscription is not registered to use namespace Microsoft.DataFactory" 
	service="microsoft.datafactory" 
    resource="datafactories,factories"
    authors="spelluru"
    displayOrder="1"
    selfHelpType="resource"
	cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>

# Error: The subscription is not registered to use namespace 'Microsoft.DataFactory'

## **Recommended steps**
If you receive this error, the Azure Data Factory resource provider has not been registered for your subscription.
One way to register the provider is to create a data factory using the Azure portal UI.  Another is with powershell, like this: 

1. Launch Azure PowerShell. 
2. Login to your Azure account using the following command: **Login-AzureRmAccount** 
3. Run the following command to register the Azure Data Factory provider: **Register-AzureRmResourceProvider -ProviderNamespace Microsoft.DataFactory**

## **Recommended documents**
[Resource providers and types](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services#resource-providers-and-types)
