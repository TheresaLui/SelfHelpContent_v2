<properties
	pageTitle="Check P2SLogsTable"
	description="Check P2SLogsTable"
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
	articleId="f3bfb1bc-130b-4124-aab0-51f3c998bf33"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check RCA for IKEv2 or OpenVpn clients on P2SLogsTable

IKEv2 and OpenVPN protocols are handled by an Azure Specific driver on the Gateway, which has always on logging to Jarvis/Kusto enabled by default.

Such logging is available at the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B)

In case of IKEv2 you can also leverage the [IkeLogsTable](https://jarvis-west.dc.ad.msft.net/A5B239BD).

## Recommended Steps

1. Review the diagnostics at the time of the issue and try to identify an error code from the logs
2. Consult a TA if you are unable to find a specific error code from the logs.
