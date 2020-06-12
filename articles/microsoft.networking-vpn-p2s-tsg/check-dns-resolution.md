<properties
	pageTitle="Check if VPN Client can Resolve VPN Gateway FQDN"
	description="Check if VPN Client can Resolve VPN Gateway FQDN"
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
	articleId="cfea7a48-7440-4c42-b738-1deae11f74d9"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to check if VPN Client can Resolve VPN Gateway FQDN


## Recommended Steps

1. Check if the VPN Gateway address can be resolved
   1. Go to ASC > Resource Explorer and select the VPN gateway
   1. Copy the GatewayID
   1. Open [Get Gateway](https://jarvis-west.dc.ad.msft.net/?page=actions&acisEndpoint=Public&selectedNodeType=3&extension=Brooklyn&group=Gateway%20Service%20Operations&operationId=getgateway&operationName=Get%20Gateway&inputMode=single&params={"gatewayid":null}&actionEndpoint=Brooklyn%20-%20Prod&genevatraceguid=834f4699-2014-4939-bebe-2740adc95585) from Jarvis Actions and search for the GatewayID
   1. From the "Get Gateway" output identify the **HostedServiceName**
   1. The FQDN of the gateway will be in the form of _HostedServiceName.vpn.azure.com_
2. Alternatively, customer can check on their side
   1. Find the FQDN of the Azure Gateway in the VpnSettings.xml file contained in the VPN package.
   1. This is in the form of _HostedServiceName.vpn.azure.com_
3. Once Gateway FQDN is identified perform **nslookup** from a command prompt to verify if the gateway IP address can be resolved.

Working example:
~~~
C:\Users\administrator>nslookup azuregateway-ced1006d-062f-41d9-874c-a71d135c5962-807ed9db6637.vpn.azure.com

Non-authoritative answer:
Name:    azuregateway-ced1006d-062f-41d9-874c-a71d135c5962-807ed9db6637.vpn.azure.com
Address:  40.115.164.54
~~~
