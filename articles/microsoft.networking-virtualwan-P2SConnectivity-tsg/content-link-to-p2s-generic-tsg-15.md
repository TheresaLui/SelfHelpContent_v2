<properties
	  pageTitle="link to P2S generic TSG"
	  description="link to P2S generic TSG"
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
	  articleId="d26cd20f-5e7c-4349-97e7-d32a74d41367"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# link to P2S generic TSG

We could exclude Name resolution issues, the client is pointing to the correct GW, but it's unable to connect.

To proceed further, please take note of the kind of P2S settings are configured on the considered P2S GW,you can access these by reviewing the relevant *VPNserverConfiguration* associated with the GW itself.

Finally, load in ASC the Inner MS-owned subscription hosting the P2S Gateway to access the GW's properties as if it was a standard Brooklyn GW:

-From the P2SVPNGateways section, select the considered P2S GW

-Scroll down to *P2S VPN Gateway Child gateways*

-In the column *Child Virtual Network Gateway Note* you will find a message like *Please add child virtual network gateway subscription: xxxxx to Resource explorer and then access this link*

-Follow such instruction: add the subscription to ASC, and pin it to the case

-Once done, you can now directly click on the link in *Child Virtual Network Gateway*

By doing this, you can now treat this P2S GW as a standard Brooklyn GW (You can review Get-GW outputs, collect Diagnostics, access Visual Debugging dashboards, etc...)

With all these preliminary actions done and info collected please proceed further with ***P2S TSG***.

Please consider that the ***P2S TSG*** could contain some scenarios not applicable to the vWAN case (i.e. all the troubleshooting branch for SSTP), but it will be good to cover the majority of the most common problems.



