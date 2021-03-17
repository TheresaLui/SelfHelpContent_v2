<properties
	  pageTitle="Recreate Connection Object"
	  description="Recreate Connection Object"
      service="Microsoft.network"
      resource="Microsoft.network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="8e93b845-58ea-41f5-9c39-5378176fa5ca"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Recreate Connection Object

The connection object is the bridge between the VPN gateway and the VNET. There will occasionally be issues with the connection object which could result in important information such as routes not being passed along from the gateway to the VMs within the VNET. Recreating the gateway is a quick and easy way to resolve these types of issues. 

# Recommended Steps

1. Navigate to the VPN gateway.
2. Select the option for "Connections" within the gateway's blade.
3. Select the correct connection.
4. Delete connection.
5. Recreate connection with same configuration. 
	
# Recommended Documents

1. (Creating a VPN Connection) [https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal#CreateConnection]

