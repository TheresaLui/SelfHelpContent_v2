<properties
	pageTitle="Windows hotfixes needed"
	description="Windows hotfixes needed"
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
	articleId="4851ee35-87b5-4038-866b-3310eb06205b"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check for Windows limitations and hotfixes for IKEv2

OS versions prior to Windows 10 are not supported and can only use SSTP or OpenVPN. Windows 10 requires a hotfix to be applied and a registry key to be added to correctly support IKEv2

## Recommended Steps

1. Review [IKE and SSTP KB for Windows 10](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#does-azure-support-ikev2-vpn-with-windows) for information about hotfix and registry setting requirements
2. Validate the customer point-to-site client is running supported versions
