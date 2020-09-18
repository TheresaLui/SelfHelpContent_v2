<properties
	pageTitle="Connect to Storage Firewall on different AD Tenants"
	description="Connect to Storage Firewall on different AD Tenants"
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
	articleId="cb823fe2-776a-4eb0-8e9d-f2ab7044ff84"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect to Storage Firewall on different AD Tenants

## Issue Description

Scenario with Customer with multiple Subscriptions on different AD Tenants wanting to connect a VM to Storage Account with firewall Enabled

## Symptoms

Resources cannot connect over separate AD Tenants

## Solutions

### Solution 1

The capability to configure Storage Firewall rules, which allow subnets from a cross-tenant VNet to access a Storage Account, was released in Jun/Jul 2019. See [**Configure Azure Storage firewalls and virtual networks - Grant access from a virtual network** ](https://docs.microsoft.com/azure/storage/common/storage-network-security#grant-access-from-a-virtual-network) for details.

This needs to be configured using Azure PowerShell or CLI.

### Solution 2

1. In the Subscription of the storage create an NVA (Network Virtual Appliance) and Vnet for the NVA.
2. Create the [service endpoint](https://docs.microsoft.com/azure/virtual-network/tutorial-restrict-network-access-to-resources) for the storage on the Vnet.
3. In the subscription of the VM create routing to send traffic to the NVA.

Follow steps to help with [network virtual appliance](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet) and routing of traffic.

This scenario will send all traffic on the subnet the VM is on to the IP address of the NVA (network virtual Appliance) and then access the storage.

If this did not solve your issue, please restart the troubleshooter and choose the Generic Issues Troubleshooting option.