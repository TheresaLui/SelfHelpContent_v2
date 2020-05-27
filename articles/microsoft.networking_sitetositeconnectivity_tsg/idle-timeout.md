<properties
	pageTitle="Idle Timeout"
	description="Idle Timeout"
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
	articleId="a3b5d06a-c424-48ab-8e13-e3441bc0c44f"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Idle Timeout

## **Recommended Steps**

* By design, if there is no traffic sent into the tunnel, the Policy Based Gateway will drop the connection after 5 minutes of inactivity.
* Review the wfpdiag.txt during the issue.
* When you see the sequence: Received Expire Notification -> Deleting QM its the driver on the VPN gateway initiating the QM Delete after 5 minutes idle timeout (dont be misled by the received wording in the log, this isnt received from on-premises)
  