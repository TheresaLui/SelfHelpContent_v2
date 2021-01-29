<properties
	pageTitle="How to check for the impacted service"
	description="How to check for the impacted service"
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
	articleId="53ad0019-31db-4082-819c-b8c6aede75a5"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check for the impacted service

### Overview

Azure Storage provides a layered security model. This model enables you to secure and control the level of access to your storage accounts that your applications and enterprise environments demand, based on the type and subset of networks used.

When the Azure Firewall is turned on, the Storage Account blocks incoming requests for data by default, unless the requests:
1. Originate from a service operating within an allowed Azure Virtual Network (VNet) 
2. Originate from a service operating within an allowed public IP address
3. Originate from a service that is part of the [**Microsoft Trusted Services** / **Exceptions**](https://docs.microsoft.com/azure/storage/common/storage-network-security#exceptions)

Please continue the workflow by selecting the most appropriate issue your customer is experiencing.
