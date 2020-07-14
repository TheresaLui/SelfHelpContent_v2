<properties
	pageTitle="Check Protocol Split"
	description="Check Protocol Split"
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
	articleId="8f7f8bfa-899c-48ea-adf4-e2c9c58f5cd9"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to determine which protocol is being used when multiple are enabled

When more than one client protocol is enabled, the Point to site range may be divided between the two protocols.

If you experience that one protocol is working and the other isn't, **the easiest workaround is to suggest customer to only configure the protocol that is working fine for them.**

## Recommended Steps

1. When using SSTP + IKEv2
   1. The first half of the range is assigned to SSTP clients
   2. The second half of the range is assigned to IKEv2 clients
   3. Inspect the VPN client IP addresses assigned to connecting clients and try to determine whether those are coming from SSTP or IKEv2. 
2. When using IKEv2 + OpenVPN the address range is NOT split. But pool is shared between the two protocols.
   1. The only way to tell whether a certain IP is assigned by IKEv2 or OpenVPN is to check the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B).
