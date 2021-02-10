<properties
	  pageTitle="Further DNS checking"
	  description="Further DNS checking"
      service="Microsoft.Network"
      resource="Microsoft.Network/VirtualWans"
	  authors="Danieleg"
	  ms.author="Danieleg"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="23c937f6-e012-49dc-9ff3-f8553ddea53d"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Further DNS checking

The name resolution of the P2S GW FQDN doesn't match with the P2S GW VIP

Try attempting same name resolution from your laptop, and make tests from different clients using different public DNS servers.

If the name resolution works fine from other clients, and using different public DNS servers, the issue could be with the specific DNS server used by the tested client, please guide customer to proceed troubleshooting in that direction.

If the considered vWAN had multiple HUBs with P2S GW deployed, please check in ASC if the resolved IP belonged to any of those.

(**Note**: You can check the P2S-HUBs where this VPN User-configuration is applied directly from ASC: 
Access the section of the considered P2SVPNGateway --> Click on its *VPNServerConfiguration* Once loaded, scroll down to *P2S VPN Gateways* field.
That field contains links to the list of all the P2S GWs where this VPN-config has been applied, you can check all the VIPs of all the GWs and validate if the resolved VIP is effectively mapped to an unexpected HUB.)

