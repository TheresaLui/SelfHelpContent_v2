<properties
	pageTitle="Check for VPN Gateway Failures"
	description="Check for VPN Gateway Failures"
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
	articleId="6425a2de-280f-4841-9387-d032c36f8080"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check for VPN Gateway Failovers or Issues

Check for gateway noteworthy events at the time of the issue using ASC insights, NetVMA or GatewayTenantLogsTable.

## Gateway Failover (most common scenario)

1. There might have been a gateway failover, caused by Maintenance or any other reason on the Gateway itself
2. GatewayTenantLogs indicate failover events, and the same can also be seen in NetVMA (you will notice the instance starting to listen on port 8081 has changed)
3. In such circumstances, **all point to site clients are disconnected by design**
4. We do not support Point to Site VPN to connect at boot or to re-connect automatically after disconnection. These features may be available at the client OS side but not supported by Azure.

***Note***: Ensure that "Let apps run in the background" is enabled for all Windows P2S clients as well.

## Other Gateway Issues 

If you identify another issue on the logs other than a Gateway Failover, you might be observing an outage on the gateway itself. Engage a TA for further troubleshooting.

## Client Issues

Sometimes it may be the client having issues and triggering a VPN disconnection. In that case we can:

- recommend the customer to collect captures during the next occurrence of the issue and identify which side (client or gateway) terminated the connection
- inspect the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B)

## **Recommended Documents**

* [Disconnected by design during gateway failover](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-highlyavailable)
* [NetVMA](https://netvma.trafficmanager.net)
* [Gateway Tenant Logs](https://jarvis-west.dc.ad.msft.net/?page=logs&be=DGrep&time=2018-11-01T14:15:00.000Z&offset=~5&offsetUnit=Minutes&UTC=true&ep=Diagnostics%20PROD&ns=BrkGWT&en=GatewayTenantLogsTable&scopingConditions=%5b%5b%22Tenant%22,%22c688c9853f2e41eeb777c2e096dafa4d%22%5d%5d&conditions=%5b%5d&clientQuery=orderby%20preciseTimeStamp%20asc%0A&chartEditorVisible=true&chartType=Line&chartLayers=%5b%5b%22New%20Layer%22,%22%22%5d%5d%20")
* [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B)
