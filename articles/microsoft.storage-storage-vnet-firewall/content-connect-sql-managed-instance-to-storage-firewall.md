<properties
	pageTitle="Connect SQL Managed Instance to Storage Firewall"
	description="Connect SQL Managed Instance to Storage Firewall"
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
	articleId="21466696-a5b5-46c3-88ff-dd5c78b32ccd"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connect SQL Managed Instance to Storage Firewall

## Issue Description

Scenario connecting SQL Managed Instancee to storage account within the same region with Storage Firewall enabled.

## Symptoms:

SQL Managed Instance traffic is being blocked by the Storage Account Firewall as private IPs cannot be whitelisted.

## Solution(**Preferred**):
Please follow the steps below to <u>deploy Azure SQL Managed instance into a VNET</u> and finally <u>whitelist the VNET/Subnet within the Storage Firewall</u>.

1. Integrate Azure SQL Managed Instance into a VNET. Choose between existing VNET or new VNET:
    1. [Create a **new virtual network** for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template)
    2. [Configure an **existing virtual network** for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-existing-add-subnet)
2. [**Whitelist the VNET within the Storage Account Firewall**](https://docs.microsoft.com/azure/storage/common/storage-network-security#managing-virtual-network-rules). This will also configure Microsoft.Storage Service Endpoint for the VNET/Subnet.

## Workaround

Move Storage to a different region and then whitelist the public IP for the Managed Instance. 

**Note:** **The Solution above is the preferred approach**. This alternative is a workaround if the details provided in the Solution above are not possible to be perfomed by the customer. 
  1. First create a Storage Account in another region from your Managed Instance (e.g. East Us for Managed Instance and East US 2 for Storage).
  2. Now we get the [Managed Instance NAT Public Address](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-management-endpoint#finding-management-endpoint-public-ip-address) (this is dynamic but doesn?t change often unless the backend decide to move the cluster which you will be notified before that happens)
      1. Run nslookup on Managed Instance host name "nslookup mi-demo.xxxxxx.database.windows.net"
          1. Go to the Managed Instance Overview and copy the Host name
      2. Next you copy the trxxx.eastus1-a.worker.vnet.database.windows.net name from the result and run another nslookup without the ".vnet" in it (e.g ?nslookup trxxx.eastus1-a.worker.database.windows.net ). The resulted IP address will be the NAT Public Address.
  3. Now we would need to whitelist the NAT Public IP on your new Storage created in another region. You will also need to whitelist the public IP for the SSMS to be able to do a restore.
  