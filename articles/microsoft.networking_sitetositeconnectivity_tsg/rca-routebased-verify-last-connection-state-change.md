<properties
	pageTitle="Verify last Connection State change if any in BrkGwt &gt; TunnelEventsTable"
	description="Verify last Connection State change if any in BrkGwt &gt; TunnelEventsTable"
	service="microsoft.network"
	resource="vpnGateways"
	authors="riturajc"
	ms.author="arshads, riturajc, sushrao"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e168fe02-ea98-4fda-a2bd-a1c3b0b8d866"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Verify last Connection State change if any in "BrkGwt/TunnelEventsTable"

## **Recommended Steps**

* Verify last Connection State change if any in "BrkGwt/TunnelEventsTable"

* Identify when the disconnection happened by reviewing the output of TunnelEventsTable or the Tenant Tunnel Stats from ASC Visual DebuggingIdentify a "TunnelStateChangedToDisconnected" eventIdentify the values of IsPlannedFailover and TunnelStateChangeReason columnsIfisPlannedFailover = true this normally indicates maintenance, or that the customer intentionally executed a Gateway Reset. In both these circumstances, the TunnelStateChangeReason should be either of "GlobalStandbyChanged", "StandbyChanged", "Locally Triggered" or "DPD timed out".IfisPlannedFailover = false the disconnection happened because of an issue or intentional configuration change (not maintenance)*
​
*<Value Name="Unknown" Value="0" /> This is catch all.*

*<Value Name="ServiceTriggered" Value="1"/> This is seen during an Brooklyn Update \ Host Maintenance Connection was triggered due to service like either 2 minute timer or any operation which called connect*

​*<Value Name="DataTriggered" Value="2" /> If driver receive a packet which needs to send over tunnel but tunnel is disconnected then we trigger the connect.*

*<Value Name="UserTriggered" Value="3" /> Connection triggered due to config change or older api of connect/disconnect (it is deprecated)*

​*<Value Name="RemoteTriggered" Value="4" /> Connection was started from remote side.*

​*<Value Name="RemoteCrashTriggered" Value="5" /> Remote side started the connect whereas tunnel was already connected. In this case we assume remote side is crashed restarted and we disconnect and accept the new connection.*

## **Recommended Documents**