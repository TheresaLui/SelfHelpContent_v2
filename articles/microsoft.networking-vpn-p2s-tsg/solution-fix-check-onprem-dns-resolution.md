<properties
	pageTitle="Solution for customer cannot perform DNS resolution of on-prem resources"
	description="Solution for customer cannot perform DNS resolution of on-prem resources"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="192c6846-7739-4692-9efc-b65e835553a8"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

We found that the DNS queries are going to Azure instead of the on-premises DNS servers. 

## Recommended Steps

1. Have your network administrator make sure that the DNS server on Azure has means of performing successful DNS resolution for external resources (for example by having conditional forwarders in place towards on-premises).



