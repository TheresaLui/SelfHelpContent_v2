<properties
	  pageTitle="debug client side name resolution"
	  description="debug client side name resolution"
      service="Microsoft.Network"
      resource="Microsoft.Network/VirtualWans"
	  authors="Danieleg"
	  ms.author="Danieleg"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="4947ffb7-303e-4f5b-b39e-610919431023"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# debug client side name resolution

The P2S GW FQDN in the XML configuration package is matching the FQDN value/s found in ASC for the considered P2S GW.

We now need to validate name resolution from the customer's test client.

Please ask customer to try resolving that FQDN from the test client:

Open a CMD prompt
Launch: **NSLOOKUP *FQDN* 8.8.8.8**

[Note: *make sure that in customer's environment it's possible to perform external DNS queries to public DNS resolvers, like the query above. This will eliminate from the picture any local DNS issue*]

