<properties
	pageTitle="Check if the failure was a planned maintenance using the Tunnel Events Table"
	description="Check if the failure was a planned maintenance using the Tunnel Events Table"
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
	articleId="11169d1d-492c-4d71-8b6f-ee1241013dd3"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# How to check if the failure was a planned maintenance using the Tunnel Events Table

## **Recommended Steps**

* Identify when the disconnection happened by reviewing the output of TunnelEventsTable or the Tenant Tunnel Stats from ASC Visual Debugging
* Identify a "TunnelStateChangedToDisconnected" event
* Identify the values of IsPlannedFailover and TunnelStateChangeReason columns
* If **isPlannedFailover = true** this normally indicates maintenance, or that the customer intentionally executed a Gateway Reset. In both these circumstances, the TunnelStateChangeReason should be either of "GlobalStandbyChanged", "StandbyChanged", "Locally Triggered" or "DPD timed out".
* If **isPlannedFailover = false** the disconnection happened because of an issue or intentional configuration change (not maintenance)
