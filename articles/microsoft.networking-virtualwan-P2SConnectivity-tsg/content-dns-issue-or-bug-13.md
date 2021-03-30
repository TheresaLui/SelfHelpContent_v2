<properties
	  pageTitle="DNS issue or bug"
	  description="DNS issue or bug"
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
	  articleId="87fe1d0c-8bb9-4428-a655-ab4409c11ee5"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# DNS issue or bug

The client is unable to resolve the P2S GW's FQDN with any IP, i.e. Name Error.

Try attempting same name resolution from your laptop, and make tests from different clients using different Public DNS servers.

If the name resolution worked fine from other clients and/or from your laptop, also using different public DNS servers, the issue could be with the specific DNS server used by the tested client, please guide customer to proceed troubleshooting in that direction.

If no client through no DNS servers is able to resolve such name, the ATM profile could be facing an issue, please escalate to TA accordingly.

