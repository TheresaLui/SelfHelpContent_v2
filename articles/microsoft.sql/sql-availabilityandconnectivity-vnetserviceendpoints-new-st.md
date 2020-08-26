<properties
    pageTitle="VNeT Service Endpoints"
    description="VNeT Service Endpoints"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745439"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    articleId="29f2e1ab-bae1-4060-a8b4-8d15e0091788-new-st"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# VNet Service Endpoints

Virtual Network (VNet) service endpoint provides secure and direct connectivity to Azure services (i.e., SQL DB) over an optimized route over the Azure backbone network. Endpoints allow you to secure your critical Azure service (i.e., SQL DB) resources to only your virtual networks. Service Endpoints enables private IP addresses in the VNet to reach the endpoint of an Azure service (i.e., SQL DB) without needing a public IP address on the VNet.

Virtual network rule is a firewall security feature that controls whether the server for your databases in Azure SQL DB accepts communication that is sent from a particular subnet in the virtual network.

## **Recommended Documents**

 - [Configure a VNET](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-vnet-configuration?WT.mc_id=pid:13491:sid:32745439/)<br>
 - [Configure a VNET-to-VNET connection using Azure CLI](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-cli?WT.mc_id=pid:13491:sid:32745439/)<br>
 - [Configure a VNET-to-VNET connection using PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vnet-vnet-rm-ps?WT.mc_id=pid:13491:sid:32745439/)
