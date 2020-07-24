<properties
	pageTitle="Connect  to Web App Server Logs to Storage Firewall"
	description="Connect  to Web App Server Logs to Storage Firewall"
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
	articleId="33a8ccb6-1395-42ec-a3d8-f430fe57cc61"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect  to Web App Server Logs to Storage Firewall

## Issue Description

Scenario using connecting a **Web App Server Logs** to storage account in the same region with firewall enabled.

## Symptoms

Failing to save Web app server logs to a storage account after the firewall has been enabled

## Solution

As of 4/14/2020 there is no solution as this is a limitation that we have right now that Web Server logs cannot be uploaded to the storage account locked with Service Endpoints. There is no current ETA for this feature, for further details please review the [workitem for this](https://msazure.visualstudio.com/Antares/_workitems/edit/5127124).

## Recommended Documents

1. [https://msazure.visualstudio.com/Antares/_workitems/edit/5127124](https://msazure.visualstudio.com/Antares/_workitems/edit/5127124)
2. [https://icm.ad.msft.net/imp/v3/incidents/details/135066928/home](https://icm.ad.msft.net/imp/v3/incidents/details/135066928/home)
