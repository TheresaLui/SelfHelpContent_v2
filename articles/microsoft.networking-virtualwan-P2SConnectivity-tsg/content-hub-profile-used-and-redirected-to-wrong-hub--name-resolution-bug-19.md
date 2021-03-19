<properties
	  pageTitle="HUB profile used and redirected to wrong HUB, Name resolution bug"
	  description="HUB profile used and redirected to wrong HUB, Name resolution bug"
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
	  articleId="eba4e31e-f419-4834-92a3-e339bfc90862"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# HUB profile used and redirected to wrong HUB, Name resolution bug

Name resolution of the FQDN of a User VPN Profile of type *Virtual HUB* (i.e. *hubx.xxxxxx.vpn.azure.com* ) cannot return IP of another HUB.

If you validated that this FQDN effectively matches with the relevant HUB-level ATM profile's FQDN, this has to be a bug.

Please escalate to TA accordingly.

