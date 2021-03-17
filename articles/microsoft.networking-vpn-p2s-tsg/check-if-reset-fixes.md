<properties
	pageTitle="How to perform gateway reset"
	description="How to perform gateway reset"
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
	articleId="5675b436-12a4-4d6f-8073-da17ddec0cd2"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to perform gateway reset

* For critical customer issues or undocumented scenarios if customer isn’t interested in root cause analysis (RCA) customer can try resetting the VPN gateway as detailed here <br/>[How to perform gateway reset](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic)
* For Classic deployment gateways, please ask the customer to install *PowerShell V6.1.0* or prior and use the cmdlet:

~~~powershell
Reset-AzureVNetGateway -VNetname <name>
~~~
