<properties
	pageTitle="Connect Azure Functions to Storage Firewall"
	description="Connect Azure Functions to Storage Firewall"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a3f9c698-1832-447c-9ffd-01a99b32ff15"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect Azure Functions to Storage Firewall

## Issue Description

Scenario using connecting a **Function App** to storage account in the same region with firewall enabled.

## Symptoms

Azure Function uses an Internal IP (not outbound IP addresses) in the form of 10.x.x.x to access storage that may be subject to change.

## Solution

Below are the solutions/workarounds available to use Azure Functions Apps with Storage Firewall enabled

### A) Using Function App with VNET Integration
 
Please follow the following steps to integrate Function Apps with a VNET and whitelist it through the Storage Account Firewall.
1.  Follow steps to [Connect your Function App to your VNET](https://docs.microsoft.com/azure/azure-functions/functions-create-vnet#connect-your-function-app-to-your-vnet)
2.  [Whitelist VNET/subnets on the Storage Account Firewall](https://docs.microsoft.com/azure/storage/common/storage-network-security#managing-virtual-network-rules). In this step, Storage Service Endpoint should be enabled as well.

**Notes:**
1. Function Apps requires the Premium Plan to support VNET Integration.
2. Make sure all resources (Azure Functions, VNET, Storage) are all in the same region.

### B) Using App Service Environment(ASE)

### Using App Service Environment(ASE)

You can enable this by deploying your Function App into an App Service Environment (ASE), which will give you one **static, dedicated IP** that you can then whitelist in the Storage Firewall.

Documentation: [Azure Functions](https://docs.microsoft.com/azure/azure-functions/ip-addresses#dedicated-ip-addresses}

If this did not solve your issue, please restart the troubleshooter and choose the Generic Issues Troubleshooting option.