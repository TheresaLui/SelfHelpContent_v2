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
	  articleId="572bdf84-67dc-4fda-879f-f5deecd365bb"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution - Check customer application

If you HttpStatusCodeError, this is an indication of a customer application failure. Advise customer that they could not connect to their load balancer VIP because all VMs in their backend pool returned an invalid HTTP response and the customer should look at their application logs for additional information.

