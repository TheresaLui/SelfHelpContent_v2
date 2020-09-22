<properties
	pageTitle="DPD Timeout"
	description="DPD Timeout"
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
	articleId="b867d12f-d930-4a9e-b1aa-dff26c23323e"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# DPD Timeout

## **Recommended Steps**

* The connection was closed due to dead peer detection
* DPD packets sent by the azure gateway are not being responded
* Collect traces on the on-prem device
* If the customer’s device isn’t responding, then escalate the issue to the customer
* If we have logs/traces from the on-prem device showing that the device is receiving our traffic and correctly responding, the issue may be within the Azure infrastructure - but outside the VPN gateway scope
* Review NetVMA status for the gateway at the time of the issue:

  * If NetVMA shows suspicious behavior, the issue may be within the Azure infrastructure - but outside the VPN gateway scope.  Go to escalate.
  * If NetVMA doesn’t show suspicious activity, this might have been a short network glitch for which we can’t provide further RCA. Inform the customer that DPD timed out because of network issues. Go to Pending customer.
