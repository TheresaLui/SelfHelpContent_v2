<properties
	  pageTitle="Attempt redeploying gateway and attempting once more."
	  description="Attempt redeploying gateway and attempting once more."
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
	  articleId="76198597-fe36-4595-83c4-611d0fedff8a"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Attempt redeploying gateway and attempting once more.

Resetting an Azure VPN gateway is helpful if you lose cross-premises VPN connectivity on one or more Site-to-Site VPN tunnels. In this situation, your on-premises VPN devices are all working correctly, but are not able to establish IPsec tunnels with the Azure VPN gateways.

# Recommended Steps

1. Navigate to the VPN gateway in the Azure Portal.
2. On the VNG blade select "Reset"
3. On the Reset page, select Reset. Once the command is issued, the current active instance of the Azure VPN gateway is rebooted immediately. Resetting the gateway will cause a gap in VPN connectivity, and may limit future root cause analysis of the issue.
	
	
# Reccommended Documents

1. (Reset a VPN Gateway) [https://docs.microsoft.com/en-us/azure/vpn-gateway/reset-gateway#:~:text=In%20the%20portal%2C%20go%20to,VPN%20gateway%20is%20rebooted%20immediately.]

