<properties
	pageTitle="No IKE negotiation packets observed on the logs"
	description="No IKE negotiation packets observed on the logs"
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
	articleId="4eb89748-4cf8-45f5-9b97-3922de8fffde"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# No IKE negotiation packets observed on the logs

## **Recommended Steps**

* Please check if the on-premises device is configured only as a Responder
* In this case, even if the interesting traffic is triggered from on-premises, the tunnel would not come up unless the traffic is originating from Azure end
* If the on-premises device cannot be configured as an Initiator, then generate traffic from Azure towards on-premises to bring up the tunnel
* Ideally the on-premises device needs to be configured both as Initiator and Responder
* If there is a limitation on the third-party device, the VPN device vendor must be engaged for further assistance
* Additionally, you may review the workflow for known issues with third-party devices

## **Recommended Documents**

* [Third Party Device Troubleshooting](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/134282/VPN-Connection-Unreliable?anchor=issues-with-3rd-party-devices)
