<properties
	pageTitle="Issues configuring LDAPS"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="arluca"
	selfHelpType="generic"
	supportTopicIds="32570967"
	productPesIds="14785,16576"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="d4c09e40-a02a-4812-b0c0-6cb71e136f54"
	ownershipId="AzureIdentity_AzureActiveDirectoryDomainServices"
/>

# Issues configuring LDAPS

## **Recommended Steps**

1.	Check your domain’s health on the Azure portal: https://aka.ms/aadds-health
2.	Ensure a valid Azure AD subscription is available and Azure AD Domain Services has been enabled.
3.	The certificate required to enable secure LDAP must be obtained from a trusted public certification authority or be a self-signed certificate.
4.	Ensure the certificate follows the required guidelines: https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-configure-secure-ldap#requirements-for-the-secure-ldap-certificate

## Invalid Certificate

1.	To renew a certificate, follow the steps to create a new certificate and reupload: https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-configure-secure-ldap
2.	Check to see if your certificate follows the required guidelines: https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-configure-secure-ldap#requirements-for-the-secure-ldap-certificate


## **Recommended Documents**

-	[Configuring Secure LDAP](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-configure-secure-ldap)
-	[Troubleshooting LDAPs configuration](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshoot-ldaps)
-	[Azure AD Domain Services Troubleshooting](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting)
