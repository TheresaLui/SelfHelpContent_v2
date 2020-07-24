<properties
	pageTitle="Connect Azure SQL Data Warehouse to Storage Firewall"
	description="Connect Azure SQL Data Warehouse to Storage Firewall"
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
	articleId="5a6c70f5-c803-41df-bf43-7cb0a95c2ff9"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect Azure SQL Data Warehouse to Storage Firewall

## Issue Description

Scenario using connecting an Azure Synapse / SQL Data Warehouse with Azure Storage Firewall and VNETs.

## Symptoms:

With standard configuration, it's not possible to connect Azure Synapse / SQL Data Warehouse with Azure Storage Firewall when using Polybase.

Polybase: is the interface to access data outside of the database, even ADF uses polybase, you don't have to use it and you can use other tools but polybase is the fastest method or tool.

## Solution

Azure Storage has implemented the same feature that allows you to limit connectivity to your Azure Storage account. If you choose to use this feature with an Azure Storage account that is being used by Azure SQL Database, you can run into issues. Next is a list and discussion of Azure SQL Database and Azure SQL Data Warehouse features that are impacted by this

**Prerequisites:**

1. Install Azure PowerShell using this [guide](https://docs.microsoft.com/powershell/azure/install-az-ps).
2. If you have a general-purpose v1 or blob storage account, you must first upgrade to general-purpose v2 using this [guide](https://docs.microsoft.com/azure/storage/common/storage-account-upgrade).
3. You must have Allow trusted Microsoft services to access this storage account turned on under Azure Storage account Firewalls and Virtual networks settings menu. Refer to this [guide](https://docs.microsoft.com/azure/storage/common/storage-network-security#exceptions) for more information.


1. Follow steps described in [**Azure Synapse / SQL Data Warehouse PolyBase**](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#azure-synapse-polybase) to onboard this feature with Storage Firewall. 
     1. Creating a System assigned Managed Identitiy will be mandatory in the steps as well as assigning the correct RBAC permissions to it.

**Note:** If customer needs assistance following the above steps, please collaborate with Azure Synapse / SQL Data Warehouse team.

