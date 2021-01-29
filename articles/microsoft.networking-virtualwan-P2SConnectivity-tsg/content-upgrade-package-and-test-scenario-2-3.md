<properties
	  pageTitle="Upgrade package and test scenario 2"
	  description="Upgrade package and test scenario 2"
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
	  articleId="6316560f-30be-4565-813d-2be2803ea65c"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Upgrade package and test scenario 2

The P2S client can connect, but to the wrong HUB of the vWAN.

If not done already, please ask customer to install a fresh version of the User VPN Client configuration for any new test.

In vWAN, you could have different P2S HUBs with same user configuration applied, and the concept of *"Virtual WAN User VPN profile"* vs. "*Virtual HUB User VPN profile"* has been introduced.

*"Virtual WAN User VPN profile"* = A client profile which will make sure client can connect to the closest P2S HUB of the vWAN, in case of multiple HUBs configured for P2S.
This can be downloaded from portal, in the *User VPN Configurations* section, by selecting the desired User VPN Configuration and clicking the *Download Virtual WAN User Profile* button.

*"Virtual HUB User VPN profile"* = A client profile which will allow client to connect to a single specific HUB within the vWAN
This can be downloaded from portal, accessing the section of the desired virtual HUB, then clicking *User VPN (Point to site)*, and finally clicking the *Download Virtual HUB User Profile* button.

In this situation, customer is evidently in a multi-P2S-HUB scenario, hence it would make sense they install the *vWAN User VPN profile* if different HUBs were sharing same P2S-configuration.

In case customer was using different P2S settings for different HUBs, customer may want to install HUB-specific User VPN profiles instead.

As soon as the fresh package is installed, please test again connectivity.

