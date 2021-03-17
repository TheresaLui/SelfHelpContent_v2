<properties
	pageTitle="Troubleshooting P2S VPN and SMB shares"
	description="Troubleshooting P2S VPN and SMB shares"
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
	articleId="e0c8b8da-5f3d-4338-bff9-6f9b8e18f87d"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Troubleshoot P2S VPN and SMB Shares

This is a legacy error (haven't appeared in about 2 years because it's fixed in an older Windows 10 version)

## Recommended Steps

1. Check if the P2S client can reach the Azure VM using ICMP or RDP.
1. Check if the VM firewall is allowing inbound connections to port 445 
1. Do the protocols which depend on LSASS for authentication fail? For example: SMB protocol used for file share access could fail because of lack of access to the Kerberos KDC – as the point to site client is often located in a remote network (away from the corporate network)
   1. Solutions: Update Windows 10 client to the RS2 build for consumer (version 15063) or 
   1. Configure *HKEY_LOCAL_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Lsa\\DisableDomainCreds = 1*

## Recommended Documents

1. https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/134255/Point-to-Site-VPN-Issues?anchor=unable-to-access-the-network-shares-of-azure-vms-from-p2s-client-with-error-%22the-network-path-was-not-found%22
