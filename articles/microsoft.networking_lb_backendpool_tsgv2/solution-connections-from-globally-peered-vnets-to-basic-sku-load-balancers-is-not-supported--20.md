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
	  articleId="13ec15c4-18d3-40d9-9d57-cf421314254a"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Connections from globally peered Vnets to basic SKU load balancers is not supported.

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer backend pool connectivity issue. We have reviewed your configuration and determined your issue is due to the use of a basic SKU load balancer. Resources in one virtual network cannot communicate with the front-end IP address of a basic internal load balancer in a globally peered vnet. Please see our documentation here for more details: https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq#what-are-the-constraints-related-to-global-vnet-peering-and-load-balancers. Our suggestion is to migrate your basic load balancer to a standard SKU load balancer where this is a supported scenario. Here are the instructions of how to do it: https://docs.microsoft.com/azure/load-balancer/upgrade-basic-standard  

Best regards,

<!--/issueDescription-->

