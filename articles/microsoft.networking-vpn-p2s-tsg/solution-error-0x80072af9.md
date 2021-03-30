<properties
	pageTitle="Solution for VPN Point-to-Site client error 0x80072af9"
	description="Solution for VPN Point-to-Site client error 0x80072af9"
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
	articleId="1cb32f43-60ff-409f-8cfe-4292951507eb"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x80072af9

The error *"0x80072af9 : No such host is Known"* is a Windows error that happens when the OS is unable to determine the IP address to connect to. This is usually due to failing DNS resolution

## Recommended Steps

1. Clear the DNS client cache with *ipconfig /flushdns* and test
2. Check for DNS resolution errors and fix on-premises DNS server issue(s).
3. Check if [Cisco Umbrella](https://umbrella.cisco.com/) or [Akamai ETP](https://learn.akamai.com/en-us/webhelp/enterprise-threat-protector/enterprise-threat-protector/GUID-778840B3-82D0-4BFB-A091-91AFFE48BA48.html) software is installed on the client as it has been shown to be responsible for causing this error.

