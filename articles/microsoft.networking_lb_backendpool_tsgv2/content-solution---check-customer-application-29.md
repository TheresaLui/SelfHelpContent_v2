<properties
	  pageTitle="Solution - Check customer application"
	  description="Solution - Check customer application"
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
	  articleId="7f461f05-6fa1-4dc8-aff6-2236601aeb91"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution - Check customer application

If you HttpStatusCodeError, this is an indication of a customer application failure. Advise customer that they could not connect to their load balancer VIP because all VMs in their backend pool returned an invalid HTTP response and the customer should look at their application logs for additional information.

