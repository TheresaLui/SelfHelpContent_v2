<properties
	pageTitle="EngageTaWithSimultaneousNetworkTraces"
	description="EngageTaWithSimultaneousNetworkTraces"
	infoBubbleText="EngageTaWithSimultaneousNetworkTraces"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32589558,32584249"
	resourceTags="windows"
	productPesIds="15526"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="VnetPeeringGetTracesAndEngageResources"
	ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Collect Simultaneous Network Traces and Engage TAs

## **Recommended Steps**

1. Make note of the resources you will take the traces (Source, Destination, and any intermediary resources such as VPN gateway, application gateway or network virtual appliance)
2. Collect simultaneous network captures during TCPPING testing both ways
   1. Install [PSPing for Windows](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/171537/PsPing) or [TCPPing for Linux](http://xmodulo.com/how-to-install-tcpping-on-linux.html) on the source and destination resources.
   2. Start network captures on both source and destination resources (and any intermediary resources):        Windows: [Netsh](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pagePath=%2FTooling%2FNetsh&pageId=138467&wikiVersion=GBmaster) | Linux: [TCPdump](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pagePath=%2FNetworking%20Principles%2FTCPdump&pageId=140089&wikiVersion=GBmaster) | [Azure Gateway Diagnostic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pagePath=%2FAzure%20VPN%2FHow%20To%2FAzure%20Gateway%20Diagnostics&pageId=134103&wikiVersion=GBmaster) if applicable.
   3. Run [PSPing for Windows](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/171537/PsPing) or [TCPPing for Linux](http://xmodulo.com/how-to-install-tcpping-on-linux.html) on the source targeting the destination
   4. Stop network captures on all resources: Windows: [Netsh](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pagePath=%2FTooling%2FNetsh&pageId=138467&wikiVersion=GBmaster) | Linux: [TCPdump](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pagePath=%2FNetworking%20Principles%2FTCPdump&pageId=140089&wikiVersion=GBmaster) | [Azure Gateway Diagnostic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pagePath=%2FAzure%20VPN%2FHow%20To%2FAzure%20Gateway%20Diagnostics&pageId=134103&wikiVersion=GBmaster) if applicable.
3. Name each trace that identifies which node the trace was taken on
4. Repeat the steps above to capture another set of traces going the other direction
5. Create a DTM Workspace in Service Desk and have customer upload the files
   
### Analyze Traces (Advanced)

1. Checking for retransmits indicating dropped packets or client/server unable to handle load
   1. To isolate traffic in the captures to just a conversation by filtering on both the client and the server IP such as this. 
~~~
(ipv4.address==\<server IP\> and ipv4.address==\<client IP\>) and (Property.TCPRetransmit==1 or Property.TCPRetransmit==1)
~~~
   2. Select a TCP conversation that has retransmits and look at that conversation on all network traces using the TCP source port from the client to create a filter like: TCP.port ==50865
   3. Do you see all retransmits arriving?
      1. If so, the server may not be responding properly
      2. If not, the packets may have been dropped on the network or by the firewall

### **Engage TAs**

1. Before proceeding, ensure you have:
   1. Completed the workflow to this point
   2. Attached all logs and traces to the support case
2. Engage colleagues & Azure Networking Pod Technical Advisers via Microsoft Teams Channels
