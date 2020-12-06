<properties
	  pageTitle="Has the customer subscribed to Azure DDoS Service?"
	  description="Has the customer subscribed to Azure DDoS Service?"
      service="Microsoft.Network"
      resource="Microsoft.Network/ddosProtectionPlans"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="e655c9ba-213e-4914-9da4-679bfa6eb35f"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Has the customer subscribed to Azure DDoS Service?

DDoS Protection Standard: Not everyone has this. It can be located in ASC as a resourceType for quick identification. If you see Microsoft.Network/ddosProtectionPlans listed in ASC, it's DDoS Protection 
 **Note** it can also be in a DIFFERENT subscription (let's call it Subscription B), but tied to a Vnet in Subscription A. In this case, check the Vnet in Subscription A, which should show associated DDoS Protection Plans as an item in ASC.
DDoS Protection Basic: Everyone in Azure has this, on every VIP, for free.


