<properties
    pageTitle="Problems with a domain name verified in another Azure AD"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615418"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="a0310cd0-bff8-422c-bc62-6a48e43b43dc"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problems verifying a domain name because verified in another tenant

## **Recommended steps**

If you are getting an error that says “Domain already configured on another tenant”, please ensure that your custom domain name hasn’t already been configured on another Azure AD or Office 365. A User in your organization may have already signed up self-service with that domain name. You must remove the domain name from the existing tenant where the domain name is already verified and add it to the new Azure AD. Learn more about [How to takeover a domain name verified in another tenant](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover).

1. Education or non-profit organizations: When you try to sign-up for an new Azure offer for education or non-profit, and you get an error “tenant not found”, this may be related to the domain you are using for sign-up being verified in another tenant. In that case, you will need to takeover the tenant where the domain is already verified, with admin takeover or can proceed to add the domain with force takeover option in PowerShell. [Verifying domain name in PowerShell](https://docs.microsoft.com/powershell/msonline/v1/confirm-msoldomain).
2. Verifying a sub-domain: If you are trying to verify a sub-domain of an existing verified domain in another Azure AD with a different authentication type than the parent domain, you must remove it before changing the authentication type.  [Adding a sub-domain if root domain is already verified](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#add-subdomains-of-a-custom-domain).

## **Recommended documents**
* [How to takeover domain verified in another Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover)
* [Understanding self-service sign-up and why a domain already exists in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-self-service-signup#how-to-perform-a-dns-domain-name-takeover)
