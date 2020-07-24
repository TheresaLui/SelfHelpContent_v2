<properties
	pageTitle="Connect Azure Bot to Storage Firewall"
	description="Connect Azure Bot to Storage Firewall"
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
	articleId="d75cde9a-572f-4118-998a-14ee498cebed"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect Azure Bot to Storage Firewall

## Issue Description

Customer want to configure **Azure Bot Deployment** with Storage Account (Private network) using Storage Account Firewall feature.

## Symptoms

In general, we can use adding IP to trusted list, but it doesn?t allow to white list IP addresses which start with 10.x.x.x, but App Service Worker may use 10.x.x.x as private IP address. So we can?t get it working with this feature.

## Solution

Below are the solutions/workarounds available to use Azure Bot Deployment with Storage Firewall enabled:

### A) Azure Bot Deployment as a Trusted Service

Currently not supported.
Azure Bot service PG team confirmed that they do not have an ETA regarding the inclusion of Bot service URLs to the [Trusted Microsoft services](https://docs.microsoft.com/azure/storage/common/storage-network-security#exceptions) when adding it to the Azure storage.

### B) Using Azure Bot Deployment with VNET Integration

1. Workaround for app service is to follow below procedure to integrate app with an Azure Virtual Network
2. Bot service deployment is with app service, and now we have a bot service workaround to configure the [**app service integrated to Azure Virtual Network**](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet).
3. **Limitation** for Bot service is that we need to confirm with customer if they are using APP service plan or Consumption plan. **Only APP Service Plan can be integrated to VNET**.

## More Information

1. To improve the networking performance, some services inside a same data center will communicate via private IP addresses, Like App Service -> Storage Account. This is architecture design.
2. Storage account firewall has two network level security controls, whitelist IP and Virtual Network.
3. For whitelist IP, it doesn?t allow to whitelist IP addresses which start with 10.x.x.x, but App Service Worker may use 10.x.x.x as private IP address. So we can?t get it work with this feature;
4. For Virtual Network configuration, it works like this:
  1. Service Endpoint gives traffic an optimal route to the Storage Account service ? via VNET;
  2. Each request brings identity information of the VNET and subnet ? this is done by platform;
  3. Storage Account service will check if the identity in request matches one of those in the existing VNET list.

Here is the structure of one type Bot service (with APP service plan), confirmed with Bot service team there will be APP service deployed automatically.

Storage account is a mandatory service for deploying the Bot service. Bot service is utilizing the storage account table for deployment & functionality purpose.

