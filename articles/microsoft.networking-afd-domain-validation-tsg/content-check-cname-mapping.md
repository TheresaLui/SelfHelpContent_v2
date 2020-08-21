<properties
	pageTitle="Check if domain name is mapped to the Azure AFD name at registrar and is propagated across the Internet"
	description="Check if domain name is mapped to the Azure AFD name at registrar and is propagated across the Internet"
	service="Microsoft.Network/"
	resource="Microsoft.Network/frontDoors"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="59a6a63a-ef40-408b-9481-cf296f8da475"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if domain name is mapped to the Azure AFD name at registrar and is propagated across the Internet


Perform an nslookup on the customer domain and ensure it is pointing to an AFD domain

```shell

nslookup %CUSTOMER_DOMAIN%

```
