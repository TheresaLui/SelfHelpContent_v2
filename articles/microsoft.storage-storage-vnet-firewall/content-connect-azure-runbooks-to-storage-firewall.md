<properties
	pageTitle="Connect Azure Runbooks to Storage Firewall"
	description="Connect Azure Runbooks to Storage Firewall"
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
	articleId="2c23db2e-6a26-4cd5-95d8-8cf64c3a7799"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect Azure Runbooks to Storage Firewall

## Issue Description

Scenario using connecting an **Azure Runbook** to Storage Account in the same region with Firewall enabled.

## Symptoms

It?s not possible to access storage from the Runbook as the IP Address of the sandbox keeps on variating and hence it cannot be whitelisted.

## Solution

Below are the solutions/workarounds available to use Azure Runbooks with Storage Firewall enabled:

### A) Azure Automation/Runbooks as a Trusted Service

Currently not supported.

Customer Feedback submission: [https://feedback.azure.com/forums/217298-storage/suggestions/33462937-whitelist-all-microsoft-services-in-storage-accoun](https://feedback.azure.com/forums/217298-storage/suggestions/33462937-whitelist-all-microsoft-services-in-storage-accoun)

### B) Using Hybrid Runbook Worker

Currently, the best possible solution is to use an Hybrid Runbook Worker and then enable the [Storage Service Endpoint on the VNET](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) of the [Hybrid Runbook Worker](https://docs.microsoft.com/en-us/azure/automation/automation-hybrid-runbook-worker).
