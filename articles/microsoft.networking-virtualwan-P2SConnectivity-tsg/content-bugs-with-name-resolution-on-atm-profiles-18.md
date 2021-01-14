<properties
	  pageTitle="Bugs with name resolution on ATM profiles"
	  description="Bugs with name resolution on ATM profiles"
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
	  articleId="47b1a2ce-ff85-4fc8-ba6f-ffb8578f7ced"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Bugs with name resolution on ATM profiles

The resolved IP doesn't belong to any specific P2S GW's VIP between all the P2S GWs of the vWAN, or customer is using *"HUB user VPN configuration"* and the resolved IP is the one of an unexpected HUB's GW.

These would be both bugs.

Please engage TA for validating possible alternatives.

