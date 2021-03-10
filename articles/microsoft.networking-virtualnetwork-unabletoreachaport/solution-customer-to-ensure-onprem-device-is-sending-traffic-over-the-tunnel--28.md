<properties
	  pageTitle="Customer to ensure onprem device is sending traffic over the tunnel."
	  description="Customer to ensure onprem device is sending traffic over the tunnel."
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
	  articleId="d866c705-68cd-4b5c-9934-ab5a8f640336"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Customer to ensure onprem device is sending traffic over the tunnel.

<!--issueDescription-->

Our troubleshooting efforts and the packet capture review has shown that traffic is successfully leaving the azure VPN gateway in route to your local routing device. Please confirm that your device is not mistakenly discarding this traffic. This is commonly the result of misconfigured ACLs. We recommend running a full packet capture on your device to confirm the possibility of any traffic being dropped by rules.

<!--/issueDescription-->

