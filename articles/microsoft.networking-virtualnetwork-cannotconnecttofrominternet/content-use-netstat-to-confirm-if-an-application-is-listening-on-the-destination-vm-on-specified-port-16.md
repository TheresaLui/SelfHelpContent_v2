<properties
	  pageTitle="Use Netstat to confirm if an application is listening on the destination VM on specified port"
	  description="Use Netstat to confirm if an application is listening on the destination VM on specified port"
      service="Microsoft.network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="257138ee-05ee-455a-b39a-0dfd47354080"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Use Netstat to confirm if an application is listening on the destination VM on specified port

"Use Netstat to confirm if an application is listening on the destination VM on the port specified by the customer.

## Recommended Steps

1. Ask the customer to run Netstat on the destination VM to confirm if an application is listening on the destination port.
 
 netstat -an | find "<port number>"

Example:
netstat -an | find ""8080""

If netstat is returning an empty response, this means that no application is listening on this port.

