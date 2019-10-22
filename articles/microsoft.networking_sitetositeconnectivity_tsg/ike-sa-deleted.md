﻿<properties
	pageTitle="IKE SA Deleted Error"
	description="IKE SA Deleted Error"
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
	articleId="7223b7a3-e982-43de-a303-6b747ccd9af0"
/>

**IKE SA Deleted Error**

* We were in a process of re-establishing a Security Association, but the on-prem device sent a Delete before we were able to complete the rekey.
* Identify from IKElogsTable if there is more detail about the malformed packet
* Verify that the customer’s device is in the list of supported VPN devices and that its configuration matches the one linked in the official documentation
* If the customer is using Cisco, Juniper or Ubiquiti devices you can also download the VPN device script from Azure to match the configuration exactly

### Public Links

1. [Supported VPN devices](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpn-devices)
2. [VPN Device Scripts](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-download-vpndevicescript)
