<properties
	pageTitle="Solution for SMB connectivity issue"
	description="Solution for SMB connectivity issue"
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
	articleId="1b0ef6e2-8cd8-477d-a1b5-ba569f2a1665"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for SMB connectivity issue

The following steps are needed to find the solution to the SMB connectivity issue.

## Recommended Steps

1. Check if the P2S client can reach the Azure VM using ICMP or RDP.
1. Check if the VM firewall is allowing inbound connections to port 445 
1. Do the protocols which depend on LSASS for authentication fail? For example: SMB protocol used for file share access could fail because of lack of access to the Kerberos KDC – as the point to site client is often located in a remote network (away from the corporate network) 
   1. Solutions: Update Windows 10 client to the RS2 build for consumer (version 15063) or 
   1. Configure *HKEY_LOCAL_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Lsa\\DisableDomainCreds = 1*

