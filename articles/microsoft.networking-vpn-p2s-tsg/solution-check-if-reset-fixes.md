<properties
	pageTitle="solution-check-if-reset-fixes"
	description="solution-check-if-reset-fixes"
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
	articleId="00dce9f5-8eea-40f1-99b4-af7a1ba7d225"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution perform gateway reset

We found that resetting the VPN gateway resolved the issue. Normally we reserve this for critical issues or undocumented scenarios where you are not interested in root cause analysis (RCA).  

## Recommended Steps

1. For 'Classic' deployment gateways, install *PowerShell V6.1.0* or prior and use the cmdlet:

~~~powershell
Reset-AzureVNetGateway -VNetname <name>
~~~

## Recommended Documents

* [How to perform gateway reset](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic)
