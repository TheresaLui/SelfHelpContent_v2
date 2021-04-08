<properties
	pageTitle="Solution for SQL Service Endpoints"
	description="Solution for SQL Service Endpoints"
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
	articleId="dfad5205-16f0-4ec2-a559-a4c6cb7fff7e"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for connecting Point-to-Site clients to SQL Service Endpoints

Azure SQL has the option to limit access to database to certain VNets/Subnets, and to deny access to Database from the Internet.

Service Endpoints are enabled per Service (e.g., Storage, SQL, etc.) on the necessary VNets/Subnets. You can enable Service Endpoints on the **GatewaySubnet**.

Access to database is denied for remote Point-to-Site users by design. However, VMs in the Vnet can be configured to have access to database.


## Recommended Steps

Follow these steps to properly enable Azure SQL to work over Service Endpoint for Point-to-Site clients.

1. From the Virtual Network portal page, access the **Service Endpoints** blade and enable them on the **GatewaySubnet**
2. From the Azure SQL firewall configuration, enable access to **GatewaySubnet**.
3. Locate your SQL server IP address using the **nslookup.exe** command. (For example, run **nslookup XXX.database.windows.net**)
4. Add the database IP address to custom routes using the **-CustomRoute** parameter in **Set-AzVirtualNetworkGateway**. See [these recommendations](https://docs.microsoft.com/Azure/vpn-gateway/vpn-gateway-p2s-advertise-custom-routes)
5. In the Azure SQL settings, firewalls, and virtual network, switch the [Connection Policy](https://docs.microsoft.com/en-us/azure/azure-sql/database/connectivity-architecture#connection-policy) to **Proxy**

## Recommended Documents

* [Use virtual network service endpoints and rules for servers in Azure SQL Database](https://docs.microsoft.com/en-us/azure/azure-sql/database/vnet-service-endpoint-rule-overview)
* [Azure SQL Database connectivity architecture](https://docs.microsoft.com/en-us/azure/azure-sql/database/connectivity-architecture)
* [Advertise custom routes for P2S VPN clients](https://docs.microsoft.com/en-us/Azure/vpn-gateway/vpn-gateway-p2s-advertise-custom-routes)
