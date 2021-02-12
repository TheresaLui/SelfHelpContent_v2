<properties
	pageTitle="IKE Timeout"
	description="IKE Timeout"
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ebb6b8c3-d6f6-4a25-8547-b63fdbf1e9bb"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# IKE Timeout

## **Recommended Steps**

Remote site is unreachable.

* Verify that the on-prem device IP address is correct, and the device receives IKE packets sent by the azure gateway and is responding
* If the customer’s device isn’t responding please inform the customer
* The connectivity issues can be due to Asymmetric routing when multiple network paths exist from On-Prem to Internet and if an on-prem stateful firewall is dropping the incoming traffic from Azure. More details on Asymmetric routing is documented at the link below
* If we have logs/traces from the on-prem device showing that the device is receiving our traffic and correctly responding, the issue may be within the Azure infrastructure - but outside the VPN gateway scope

## **Recommended Documents**

* [Express Route: Asymmetric Routing](https://docs.microsoft.com/azure/expressroute/expressroute-asymmetric-routing)
