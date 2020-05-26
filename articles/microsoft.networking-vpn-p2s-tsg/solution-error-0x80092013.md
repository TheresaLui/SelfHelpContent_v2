<properties
	pageTitle="Solution for VPN Point-to-Site client error 0x80092013"
	description="Solution for VPN Point-to-Site client error 0x80092013"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="fbad1c03-d9c3-4efb-a20c-4edd8824eee1"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x80092013

The error *"Error 0x80092013: The revocation function was unable to check revocation because the revocation server was offline"* is caused by an incorrect Proxy set up within your environment or is an on-premises network issue. The certificate revocation check function requires access to http://crl3.digicert.com/ssca-sha2-g1.crl and http://crl4.digicert.com/ssca-sha2-g1.crl.


## Recommended Steps

1. Have your local network administrator ensure the follow URLS are allowed your network proxies and edge firewalls: http://crl3.digicert.com/ssca-sha2-g1.crl and http://crl4.digicert.com/ssca-sha2-g1.crl.
