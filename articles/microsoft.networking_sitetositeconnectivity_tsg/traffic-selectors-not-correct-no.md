﻿<properties
	pageTitle="Use of traffic selectors"
	description="Use of traffic selectors"
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
	articleId="535d4568-4172-4732-91dd-f67bf5aac1f5"
/>

# Use of traffic selectors

* If narrow traffic selectors are being used, it means that the Azure VPN Gateway is configured to use narrow traffic selectors between the virtual network address space and the local network gateway address space.
* Review IkeLogs/ SeamlessTunnelServiceTraceTable in ASC or Jarvis/Kusto from the time of the issue to see which side is using traffic selectors.
* Ensure traffic selectors on both side are matching (using the same subnets)
