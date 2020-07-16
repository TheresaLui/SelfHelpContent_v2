<properties
	pageTitle="Perform Sync Network Operation for Webapp resources"
	description="Perform Sync Network Operation for Webapp resources"
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
	articleId="a21de0d2-231e-4ad9-b338-42d72e8f37f7"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check Sync Network Operation for Webapp resources

1. Have customer perform **Sync Network Operation** in the WebApp resource in the Azure portal.
2. Sometimes the Web Apps do not connect because of certificate mismatch.
3. To fix this, you need to perform a **Sync Network operation** on the Web App that has the effect of re-configuring Point to Site on it – including all certificates.

## Additional steps if the WebApp needs to reach a remote destination crossing a site to site tunnel

1. Check if the on-prem VPN device has a route for the P2S client IP range
2. Ensure that customer is attempting transit routing - that routes exist for the remote networks

## **Recommended Documents and limitations**

* [Sync Network Operation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-sync-network-configuration)
* [VPN integration](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#accessing-on-premises-resources)
