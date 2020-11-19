<properties
	pageTitle="Port 443 down"
	description="Port 443 down"
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
	articleId="f9c9f676-dc3f-4dbd-a4c2-666d8c82d0be"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Gateway not listening on port 443

If SSTP is enabled and Gateway is not responding, we are facing an issue on the Gateway in the RRAS component:

* The RRAS feature might have failed installation (known issue [6118450](https://msazure.visualstudio.com/One/_workitems/edit/6118450))
* The RemoteAccess service might have failed to start (known issue [6606537](https://msazure.visualstudio.com/One/_workitems/edit/6606537))

If you are facing any of the known RRAS issues, or some other similar variant, please reach out to a TA for further review.
It is advised for the TA to RDP into the gateway and inspect the RRAS status.
