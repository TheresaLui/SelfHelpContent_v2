<properties
	  pageTitle="Use Netstat to confirm if an application is listening on the destination VM on specified port"
	  description="Use Netstat to confirm if an application is listening on the destination VM on specified port"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="aba7931a-b428-4d29-a526-804372b2f615"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Use Netstat to confirm if an application is listening on the destination VM on specified port

Use Netstat to confirm if an application is listening on the destination VM on the port specified by the customer.

## Recommended Steps

1. Ask the customer to run Netstat on the destination VM to confirm if an application is listening on the destination port.
netstat -an | find "<port number>"

Example:
netstat -an | find "8080"

If Netstat is returning an empty response, this means that no application is listening on this port.

