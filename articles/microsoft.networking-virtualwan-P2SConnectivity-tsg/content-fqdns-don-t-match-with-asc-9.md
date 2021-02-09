<properties
	  pageTitle="FQDNs don?t match with ASC"
	  description="FQDNs don?t match with ASC"
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
	  articleId="c15fbc4b-9e6c-46b5-851f-12155bf5eaa0"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# FQDNs don't match with ASC

The GW FQDN retrieved from a freshly downloaded package is not matching with any of the FQDNs of the Azure Traffic Manager profiles (Virtual WAN / Virtual HUB) found in ASC.

This is likely a bug.

The association of a new/different P2S User VPN profile to the considered GW may fix the problem.

Please engage TA for validating possible alternatives

