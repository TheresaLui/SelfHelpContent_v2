<properties
	pageTitle="Fix Client DNS Settings"
	description="Fix Client DNS Settings"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="6496f83c-27c3-4918-bfa1-db9a6315222c"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for Fix Point to Site Client DNS Settings

We found that your point-to-site client DNS settings were incorrect.

## Recommended Steps

1. Make sure the metric of the Point to Site interface is lower (by increasing the metric of the Ethernet/Wifi adapter)
2. There is a Windows 10 OS known behavior for which the metric of the Point to Site adapter might be equal/higher than the metric of the Ethernet adapter. In that case, the client will prefer the DNS servers specified on the Ethernet adapter rather than the Azure specified DNS servers coming via Point to Site. In this scenario, the client might fail to reach Azure resources. Have your network administrator configure the right metric for the DNS server that Azure VPN is using, leveraging FQDNs or DNS forwarders/conditional forwarders which will make the point-to-site adapter preferred
3. Another option is to make sure that the DNS server specified on Ethernet adapter has means of performing successful DNS resolution (for example by having conditional forwarders in place towards Azure)



