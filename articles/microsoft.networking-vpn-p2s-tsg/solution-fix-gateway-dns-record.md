<properties
	pageTitle="Customer must add A record for VPN Gateway"
	description="Customer must add A record for VPN Gateway"
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
	articleId="20017e50-f737-4b0c-b25d-5ed87a12f1fc"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for gateway DNS not resolved by client

We found that DNS resolution of the gateway FQDN is failing. The DNS infrastructure needs to be updated to make DNS able to resolve the VPN gateway IP. The ***.vpn.azure.com** DNS zone that hosts our DNS records is publicly available on the internet.


## Recommended Steps

1. Have your network administrator fix the DNS infrastructure so DNS can resolve the IP address of the VPN gateway OR 
2. Create a Host A Record on the client's DNS Server (or hosts file) pointing the VPN Gateway FQDN to the Gateway IP