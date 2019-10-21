﻿<properties
	pageTitle="Check Brooklyn Diagnostic Logs for Route Based VPN"
	description=""
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="e5fa153c-17a6-473c-8b12-2482e52be78d"
/>

## **How to check Brooklyn Diagnostic Logs for Route Based VPN**

* Utilize the “Visual Debugging” available in ASC on VPN Gateway resource. Most of the issues may be evident from these dashboards.
* Diagnostic logs (IkeLogsTable, TunnelEvents, SeamlessTunnelServiceTraceTable) are available in ASC under the “Brooklyn Logs” tab.
* You can also collect Gateway Diagnostics in ASC from the “Diagnostics” tab.
* In some scenarios you may be required to collect these logs and diagnostics manually. In such scenarios, use the alternative steps link provided below.

### Private Links

1. [Visual Debugging of VPN Gateways](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pageId=181134)
2. [IkeLogsTable](https://jarvis-west.dc.ad.msft.net/3B96A61D)
3. [SeamlessTunnelServiceTraceTable](https://jarvis-west.dc.ad.msft.net/CAB06602)
4. [Azure Gateway Diagnostics on internal wiki](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pageId=134103)