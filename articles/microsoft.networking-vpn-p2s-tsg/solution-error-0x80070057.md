<properties
	pageTitle="Solution for VPN Point-to-Site client error 0x80070057"
	description="Solution for VPN Point-to-Site client error 0x80070057"
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
	articleId="298c70ed-fd39-4156-8f4d-e2ae00cd3951"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x80070057

The error *"Error 0x80070057: Custom script (to update your routing table) failed"* is due to a network range overlap.

The Point to Site range overlaps with the current local network range where the point to site client is at the time of connecting - not necessarily your on-premises office network but even a home network or a hotspot network depending on current client location.

The client is failing to add an additional route for the Point to Site range (since a similar route already exists).

## Recommended Steps 

Make sure that there is no overlap between the Point to Site client range listed in Azure and the local network range where the client is currently.

* Customer address space cannot overlap between Azure and Customer Premise
* Verify that the point to site client range is NOT overlapping with any of the customer’s on-premises networks
* There is no means to verify this on the Azure side
* The customer needs to choose a valid non-overlapping Point to Site IP range according to their environment

