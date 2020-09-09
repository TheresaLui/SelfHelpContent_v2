<properties
	pageTitle="Check-Port-Scanner"
	description="Check-Port-Scanner"
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
	articleId="9f3c8c4b-a62a-4c26-b213-4fbc6f5b098b"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check if the destination is responding using Port Scanner

The "host-to-guest port scanner diagnostic" is a diagnostic that passes a VM private IP and port range to the Network Watcher host agent to send TCP probes to the VM TCP ports to assess the TCP response.

## Recommended Steps

1. Go to ASC > Resource Explorer and select the destination VM or Load Balancer the customer is trying to reach.
2. Execute Port Scanner diagnostics as per the [guidelines](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/311342/ASC-Host-to-Guest-Port-Scanner-Diagnostic?anchor=using-the-host-to-guest-port-scanner)

## Recommended Documents

1. [Port Scanner Diagnostic](https://aka.ms/vmportscanner)

