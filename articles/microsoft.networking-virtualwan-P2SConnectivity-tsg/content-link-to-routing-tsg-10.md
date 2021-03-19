<properties
	  pageTitle="Link to Routing TSG"
	  description="Link to Routing TSG"
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
	  articleId="f4b3c36e-76c7-434b-8036-b66cbd497d4d"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Link to Routing TSG

The client is able to connect the P2S link with the expected P2S gateway, but it can't reach the desired destination (remote host through branch connection / VNET / etc..) even after installation of up-do-date VPN package.

In this case, the issue is likely depending on routing problems, or problems with intermediate firewalls or stateful inspectors blocking traffic.

**vWAN ROUTING TSGs** are currently under development.

Until completion, you can leverage Wiki sections dedicated to vWAN's Datapath, selecting the best-matching scenario depending on the remote destination customer is trying to connect to:

https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/400028/VWAN-Routing-TS?anchor=vwan-routing-troubleshooting-with-scenarios

