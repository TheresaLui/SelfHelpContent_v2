<properties
	pageTitle="Enabling and Disabling Azure AD Domain Services"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="eringreenlee"
	selfHelpType="generic"
	supportTopicIds="32447391"
	productPesIds="14785,16576"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="b339d2d4-efba-4292-a420-5a33c257e399"
	ownershipId="AzureIdentity_AzureActiveDirectoryDomainServices"
/>

# Enabling and Disabling Azure AD Domain Services

##**Recommended steps**
### Unable to enable AAD-DS or deployment is failing

1.	If you are using an already existing Virtual Network, check your NSG for rules that block ports needed to synchronize in Azure AD Domain Services: https://aka.ms/aadds-networking
2.	Check to see if your error message is answered in this troubleshooting guide: https://aka.ms/aadds-troubleshoot-enable
3.	Try deploying Azure AD Domain Services in a new Virtual Network.
4.	Follow the Getting Started guide on how to deploy AAD-DS: https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started


### Unable to disable AAD-DS
Azure AD Domain Services is unable to be paused. If you wish to stop using your managed domain, it must be deleted.

## **Recommended Documents**
* [Troubleshooting enabling Azure AD Domain Services](https://docs.microsoft.com/azure/active-directory-domain-services/troubleshoot)<br>
* [Azure AD Domain Services Troubleshooting](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting)