<properties
	pageTitle="Connect Azure Data Factory to Storage Firewall"
	description="Connect Azure Data Factory to Storage Firewall"
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
	articleId="af0b7813-0c58-416a-baa2-ed5ff14594b1"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect Azure Data Factory to Storage Firewall

## Issue Description

Scenario connecting an **Azure Data Factory(ADF)** with Azure Storage Firewall and VNETs.

## Symptoms

It's not possible to connect Azure Data Factory to `on-premise` storage by whitelisting Azure IP range.

## Solution

Below are the solutions/workarounds available to use Azure Data Factory with Storage Firewall and VNETs:

### Azure Data Factory as a Trusted Service

**Data Factory** is now part of **Trusted Services** in **Azure Key Vault** and **Azure Storage**. [**Integration runtime**](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime) (Azure, Self-hosted, and SSIS) can now connect to Storage/ Key Vault without having to be inside the same virtual network or requiring you to allow all inbound connections to the service. 

**Note**: Mapping Data flows does not work using the `Trusted Services` yet. We will be enabling this functionality for data flows soon.

#### Steps to connect as Trusted Service

1. Connecting to Azure Storage (using [**Azure blob**](https://docs.microsoft.com/azure/data-factory/connector-azure-blob-storage#linked-service-properties) or [**Azure Data lake Gen2**](https://docs.microsoft.com/azure/data-factory/connector-azure-data-lake-storage#linked-service-properties) linked service)
2. Grant Data Factory's Managed identity access to read data in storage's access control. For more detailed instructions, please refer [**this**](https://docs.microsoft.com/azure/data-factory/connector-azure-data-lake-storage#managed-identity).
3. Create the [linked service using Managed identities](https://docs.microsoft.com/azure/data-factory/connector-azure-data-lake-storage#managed-identity) for Azure resources authentication
4. Modify the firewall settings in Azure Storage account to select `Allow trusted Microsoft Services`?. 

**Note**: Only [Managed Identity](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity) authentication is supported when using Trusted Service functionality in storage to allow Azure Data Factory to access its data. 

### Other data integration security scenarios

1. Use the Internet to connect to data stores/ secrets store over TLS
    1.  Security : secure data using all supported **Auth** mechanism
    2. Recommendation : **Use Azure IR/ SSIS IR**
2. Use a private network/ virtual network to connect to data stores over TLS
    1. Security : secure data using **Auth** + **compute injection/ peering** with the private network
    2. Recommendation : **Use Self-hosted IR/ SSIS IR** within your Virtual Network/ Private network.

**Note**: We are actively working on adding the capability to add/ peer an Azure IR inside VNET. 

## Recommended Documents

1. [Data factory is now a trusted service](https://techcommunity.microsoft.com/t5/azure-data-factory/data-factory-is-now-a-trusted-service-in-azure-storage-and-azure/ba-p/964993)


If this did not solve your issue, please restart the troubleshooter and choose the Generic Issues Troubleshooting option.
