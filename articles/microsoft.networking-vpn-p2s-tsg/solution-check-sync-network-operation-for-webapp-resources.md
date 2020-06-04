<properties
	pageTitle="Solution Sync Network Operation for Webapp resources"
	description="Solution Sync Network Operation for Webapp resources"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="63c446be-d1ae-48df-98d7-2e5592b417e7"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for Sync Network Operation for Webapp resources

We found the cause of the connectivity issue was the Web Application did not have the current routes for the virtual network(s). Performing a 'Sync Network' operation updated the routes and resolved the connectivity issue. The steps we took are below for your reference.

## Recommended Steps

1. Perform **Sync Network Operation** in the WebApp resource in the Azure portal.

## Additional steps if the WebApp needs to reach a remote destination crossing a site to site tunnel

1. Check if the on-prem VPN device has a route for the P2S client IP range
2. Ensure that customer is attempting transit routing - that routes exist for the remote networks

## **Recommended Documents and limitations**

* [Sync Network Operation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-sync-network-configuration)
* [VPN integration](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#accessing-on-premises-resources)
