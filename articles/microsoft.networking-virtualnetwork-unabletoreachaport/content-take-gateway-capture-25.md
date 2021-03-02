<properties
	  pageTitle="Take Gateway Capture"
	  description="Take Gateway Capture"
      service="Microsoft.network"
      resource="Microsoft.network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="d22b8a6c-2d7a-4f96-836a-f0e5309eccbf"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Take Gateway Capture

Brooklyn Gateway Packet Capture is utilized to capture ESP / IKE / OVPN / unencrypted packets over the tunnel i.e. seeing source IP and port and destination IP and port like when doing pspings across the tunnel when troubleshooting Site to Site

# Recommended Steps

1. Navigate to the Diagnostics tab in of the VNG within ASC and navigate to the Brooklyn Gateway Packet Capture option.
2. Pick packet capture operation, options are start and stop
3. Select which connection object you want to capture for
4. Leave everything else blank
5. Ensure that capture software and customer repro is ready. 
6. Run the capture
7. Reproduce issue.
8. Stop capture. 

# Reccommended Documents

1. (Brooklyn Gateway Packet Capture) [https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/334173/Brooklyn-Gateway-Packet-Capture-via-ASC]

