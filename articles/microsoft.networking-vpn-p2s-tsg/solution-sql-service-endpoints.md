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

# Solution for connecting Point to Site clients to SQL Service Endpoints

Azure SQL has the option to limit access to database to certain VNets/Subnets, and deny access to DB from the Internet.

Service Endpoints are enabled per Service (Storage, SQL, …) on needed VNets/Subnets. You can enable Service Endpoints on the GatewaySubnet.

Access to database is by design denied for remote Point to Site users. At the same time, access from VMs in the Vnet is working fine.
Additional configuration steps are needed to achieve this task.

## Recommended Steps

To properly enable Azure SQL to work over Service Endpoint for Point to Site clients:
1. From the Virtual Network portal page, access the Service Endpoints blade and enable them on the GatewaySubnet
2. Enable access to GatewaySubnet from Azure SQL firewall configuration.
3. Locate your SQL server IP address using nslookup.exe command ( for example running *nslookup XXX.database.windows.net*)
4. Follow recommendations mentioned in this [public document](https://docs.microsoft.com/Azure/vpn-gateway/vpn-gateway-p2s-advertise-custom-routes) and add the database IP address to custom routes using the *-CustomRoute* parameter in *Set-AzVirtualNetworkGateway*
5. Switch [Connection Policy](https://docs.microsoft.com/en-us/azure/azure-sql/database/connectivity-architecture#connection-policy) to **Proxy** in Azure SQL Settings/Firewalls and virtual networks


## Recommended Documents

* [Use virtual network service endpoints and rules for servers in Azure SQL Database](https://docs.microsoft.com/en-us/azure/azure-sql/database/vnet-service-endpoint-rule-overview)
* [Azure SQL Database connectivity architecture](https://docs.microsoft.com/en-us/azure/azure-sql/database/connectivity-architecture)
* [Advertise custom routes for P2S VPN clients](https://docs.microsoft.com/en-us/Azure/vpn-gateway/vpn-gateway-p2s-advertise-custom-routes)
