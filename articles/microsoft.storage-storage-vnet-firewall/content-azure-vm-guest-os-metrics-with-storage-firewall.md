<properties
	pageTitle="Azure VM Guest OS Metrics with Storage Firewall"
	description="Azure VM Guest OS Metrics with Storage Firewall"
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
	articleId="ed34f8f7-25cb-40d3-8901-66bcedb3e754"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Azure VM Guest OS Metrics with Storage Firewall

## Issue Description

Guest OS Metrics and Diagnostics data in the Portal is not displayed after enabling the ?VNET and Firewall? option on Storage account.

## Symptoms

The issue is when we are able to see the Guest Metrics and The Boot Diagnostics when the Storage Firewall is turned off. However, the moment Firewall is turned on(along with the option to allow MS trusted services), we are not able to access VM Guest Metrics or the boot Diagnostics in the Portal.

## Solution

We raised this issue with Azure Monitor/Insights Product Group and they confirmed this as known scenario, **however it cannot be fixed**.

We further discussed future road-map on same and got to know that the goal is to move to alternative approach (custom metrics) which won?t have this issue.

1. There is no way to achieve the scenario with firewalled storage. The current approach of having Guest Metrics routing data to customer's Storage Account will go away in future.
2. The goal is to have WAD/LAD send custom metrics to new Diagnostics Sink - "AzureMonitorSink", which won?t have this problem (as metrics are not pushed to customer?s Storage Account at first place).
3. Custom metrics is in Public Preview, currently supporting limited regions only. Insights PG plans to support all regions of Public Azure in next ~2 months (tentative July 2019).
4. No GUI/UX to enable custom metrics from portal yet. Configuring WAD (with custom metrics) needs to be done via ARM template which can be a little cumbersome.
5. Enabling UX support in Portal i.e. modify Diagnostics Setting Blade to allow sending Guest Metrics to new pipeline (Sink "AzureMonitorSink") and make it default for newly created VMs is expected tentatively by August 2019. This should ease manual configuration efforts.
6. Once new approach is established to solve the problem, Azure Monitor PG will brainstorm transition path to new approach (for existing VMs) and later consider deprecating the old approach.

If this did not solve your issue, please restart the troubleshooter and choose the Generic Issues Troubleshooting option.