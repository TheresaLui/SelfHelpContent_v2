<properties
  pagetitle="Configuring and Managing Function Apps/VNET or Hybrid Connection&#xD;"
  description="Configuring and Managing Function Apps/VNET or Hybrid Connection"
  service="microsoft.web"
  resource="sites"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32630473"
  resourcetags=""
  productpesids="16072"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="fe08eafc-356b-4ae5-af6a-68cc5ae76f0c"
  ownershipid="Compute_AppService" />
# Configuring and Managing Function Apps/VNET or Hybrid Connection



### New VNet Integration FAQ 

* [Your app must be in an Azure App Service deployment that is capable of scaling up to Premium v2](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#new-vnet-integration)
* [You can access resources across ExpressRoute connections without any additional configuration beyond integrating with the ExpressRoute connected VNet](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#new-vnet-integration)
* [Global peering are not yet available with the new VNet Integration](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#new-vnet-integration)
* [To use your own DNS server with the new VNet integration you have to create an Application setting for your app where the name is WEBSITE_DNS_SERVER](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#new-vnet-integration)


### Existing VNet Integration  (Point-to-site) FAQ

* Existing VNet Integration does not support: Mounting a drive, AD integration, NetBios, private site access, accessing resources across ExpressRoute, accessing resources across Service Endpoints. 

* Q. Why does tcpping in the Kudu console results on "Connection attempt failed: An attempt was made to access a socket in a way forbidden by its access permissions"? <br>

	A: This could happen because the IP address you are trying to connect to is not included on the "IP ADDRESSES ROUTED TO VNET" section of the Networking blade of the App Service Plan. For more info see [Managing the VNet Integrations](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#managing-the-vnet-integrations). <br>

* Q: Why does tcpping result on "Connection attempt failed: A non-recoverable error occurred during a database lookup"? <br>

	A: This could happen because of one of the two reasons below: <br>
   
* The Point-to-Site address range in the Virtual Network Gateway has to be within the Private IPv4 address space per RFC 1918: <br>
	
	* 10.0.0.0 – 10.255.255.255
	* 172.16.0.0 – 172.31.255.255
	* 192.168.0.0 – 192.168.255.255 <br> 

* IKEV2 is selected as the "Tunnel type" of the "Point-to-site configuration" section of your Virtual Network Gateway. Change it to SSTP (SSL). For more info see: [Set up a gateway in your VNet](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#set-up-a-gateway-in-your-vnet). <br> 

* Q: Getting "Certificate sync has failed: Legacy Cmak generation is not supported for gateway id…when IKEV2 or External Radius based authentication is configured" error.<br> 
	
	A: In your Virtual Network Gateway change the "Tunnel type" from IKEV2 to SSTP (SSL) in the "Point-to-site configuration" section.

## **Recommended Documents**

* [Azure Functions networking options](https://docs.microsoft.com/azure/azure-functions/functions-networking-options)
* [Tutorial: integrate Functions with an Azure virtual network](https://docs.microsoft.com/azure/azure-functions/functions-create-vnet)
* [Integrate your app with an Azure Virtual Network](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet)
* [Azure Functions premium plan](https://github.com/Azure/Azure-Functions/blob/master/functions-premium-plan/overview.md)
* [Connecting Azure Function to an Azure VM in a VNET using Hybrid Connection Manager](https://blogs.msdn.microsoft.com/benjaminperkins/2018/05/16/how-to-azure-function-app-with-hybrid-connection/)
* [Inbound/Outbound IP addresses in Azure Functions](https://docs.microsoft.com/azure/azure-functions/ip-addresses)