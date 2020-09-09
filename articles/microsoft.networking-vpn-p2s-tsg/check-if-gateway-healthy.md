<properties
	pageTitle="Check if VPN Gateway is currently healthy"
	description="Check if VPN Gateway is currently healthy"
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
	articleId="32dcdfbf-39c8-4b7c-bec2-71a53615727a"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to check if VPN Gateway is currently healthy

1. Go to ASC > Resource Explorer and select the VPN gateway
2. Copy the Public IP address of the gateway labelled as **Gateway VIP**
3. Open a new browser window and go to **https://GATEWAY_VIP:8081/healthprobe** where GATEWAY_VIP is IP the address of the VPN gateway
4. Click on the "Not secure" area in the browser address bar
5. If the gateway is healthy and reachable, a web service will show you the name of the primary instance, the GWT version and the OS version that the gateway is running. For example:

~~~xml
<string xmlns="http://schemas.microsoft.com/2003/10/Serialization/">
Primary Instance: GatewayTenantWorker_IN_0 GatewayTenantVersion: 19.6.100.26 OSVersion: Windows Server 2012 R2 Datacenter
</string>
~~~
