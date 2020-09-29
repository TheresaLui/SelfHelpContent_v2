<properties
	pageTitle="Virtual Network selection and configuration issues"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="eringreenlee"
	selfHelpType="generic"
	supportTopicIds="32570966"
	productPesIds="14785,16576"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="3c8683aa-0d72-42d9-b126-f6446a60354b"
	ownershipId="AzureIdentity_AzureActiveDirectoryDomainServices"
/>

# Virtual Network selection and configuration issue

## Network connection issues

1.	Check your domain’s health on the Azure portal: https://aka.ms/aadds-health
2.	Check your NSG for rules that block ports needed to synchronize in Azure AD Domain Services: https://aka.ms/aadds-networking
3.	Make sure your virtual network is deployed in the same Azure Region as your Azure AD Domain Services managed domain
4.	Ensure you don’t have an existent domain with the same domain name available on the virtual network.


## **Recommended Documents**

-	[Selecting a virtual network]( https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-networking)
-	[Azure AD Domain Services Troubleshooting](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting)
