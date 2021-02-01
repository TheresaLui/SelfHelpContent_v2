<properties
	  pageTitle="Connections from globally peered Vnets to basic SKU load balancers is not supported."
	  description="Connections from globally peered Vnets to basic SKU load balancers is not supported."
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="64979278-fa2d-4683-854f-5bf6bf7328b9"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connections from globally peered Vnets to basic SKU load balancers is not supported.

* Resources in one virtual network cannot communicate with the front-end IP address of a Basic SKU internal load balancer in a globally peered virtual network
* To connect to internal load balancers from globally peered VNets, the customer must upgrade to Standard Load Balancer SKU. Currently, the customer must delete their existing load balancer and redeploy it as standard SKU as directly upgrading is not possible. The product team makes a script available to automate this available here: https://docs.microsoft.com/azure/load-balancer/upgrade-basic-standard

## Recommended Documents

* https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq#what-are-the-constraints-related-to-global-vnet-peering-and-load-balancers


