<properties
	pageTitle="Check Client DNS Settings"
	description="Check Client DNS Settings"
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
	articleId="eea1c5c3-30bd-4fc7-a8b1-85acaf198362"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check P2S and Client DNS Settings

Verify if the customer can correctly resolve Azure resources via DNS.

## Recommended Steps

1. Run **ipconfig /all** on the client to check if P2S client does not have custom DNS showing on the VPN interface. If it does not, redownload the P2S client package and re-install.
1. Have the customer check if the point-to-site client is a member of the same Active Directory domain where the destination VM is, by reviewing the output of **sysdm.cpl**. If not, the resolution is to add a host entry of the Azure VM to the local host file on the point-to-site client, or leverage FQDNs.
1. Check the VPN Point to Site adapter metric to see if it is equal/higher than the metric of the Ethernet/Wifi adapter by having the customer run this PowerShell command on the client:
 ~~~powershell
 Get-NetIPInterface
 ~~~
4. Make sure the point to site client can correctly resolve Azure resources by pinging the FQDN of an Azure Virtual Machine.
