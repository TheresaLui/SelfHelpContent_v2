<properties
	pageTitle="Connect Web App to Storage with Firewall"
	description="Connect Web App to Storage with Firewall"
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
	articleId="0f3d5a53-c053-4036-83f5-774c528be444"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect Web App to Storage with Firewall

## Issue Description

Scenario using connecting a **Web App Service** to storage account in the same region with Storage Firewall enabled.

For Web App Server logs please go one step back and select ***Web App Server logs***

## Symptoms

App service send traffic using azure data center dynamic public IP address ranges, which change every week.

## Solution

Using [**App service with VNET integration**](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet)

1. Using link above to create your App service and Vnet integration.
2. Add [**route for App Service**](https://blogs.msdn.microsoft.com/waws/2017/07/20/add-routes-to-an-azure-web-app-integrated-with-a-vnet/) to get all outbound IPs to go through Vnet
3. Add storage service endpoint to the Vnet.
4. Whitelist subnets on [**Storage Firewall**](https://docs.microsoft.com/azure/storage/common/storage-network-security)


If this did not solve your issue, please restart the troubleshooter and choose the Generic Issues Troubleshooting option.