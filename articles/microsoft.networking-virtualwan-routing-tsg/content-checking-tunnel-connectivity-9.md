<properties
	  pageTitle="Checking tunnel connectivity"
	  description="Checking tunnel connectivity"
	service="Microsoft.Network"
resource="Microsoft.network/virtualWans,Microsoft.Network/virtualwans,Microsoft.Network/virtualWans"
	  authors="lochiluk"
	  ms.author="Brwurz"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="2a1d9418-56ce-4cb8-96f8-25e11e7e7459"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Checking tunnel connectivity

In this step you'll be looking into the child gateway and see if the tunnel is up/connected by using steps below:

1) pull the child gateway ID using this link using 5th bullet point: https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/400028/VWAN-Routing-TS?anchor=required-information 
2) use the Gateway ID and use tunneleventstable from Jarvis Logs an dsee the tunnel customer is trying to connect says it's connected. (Use this link for reference and add the gateway ID: https://jarvis-west.dc.ad.msft.net/7BA2E58A)

