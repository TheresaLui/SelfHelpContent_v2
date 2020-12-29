<properties
	  pageTitle="Upgrade package and test scenario 1"
	  description="Upgrade package and test scenario 1"
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
	  articleId="b7cf38a8-b081-49ef-8bb0-a90adc3d19bb"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Upgrade package and test scenario 1

The P2S client can't connect at all to the HUB.

If not done already, please ask customer to install a fresh version of the User VPN Client configuration for any new test.

In vWAN, you could have different P2S HUBs with same user configuration applied, and the concept of *"Virtual WAN User VPN profile"* vs. "*Virtual HUB User VPN profile"* has been introduced.

*"Virtual WAN User VPN profile"* = A client profile which will make sure client can connect to the closest P2S HUB of the vWAN, in case of multiple HUBs configured for P2S.
This can be downloaded from portal, in the *User VPN Configurations* section, by selecting the desired User VPN Configuration and clicking the *Download Virtual WAN User Profile* button.

*"Virtual HUB User VPN profile"* = A client profile which will allow client to connect to a single specific HUB within the vWAN
This can be downloaded from portal, accessing the section of the desired virtual HUB, then clicking *User VPN (Point to site)*, and finally clicking the *Download Virtual HUB User Profile* button.

Ask customer to install basing on the desired connection topology they want to reach.

This can help for the configuration of the client profile, depending on the considered VPN client solution: https://docs.microsoft.com/en-us/azure/virtual-wan/virtual-wan-point-to-site-portal#configure-client 

As soon as the fresh package is installed, please test again connectivity.

