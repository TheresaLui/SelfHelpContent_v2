<properties
	pageTitle="Getting started and troubleshooting MFA"
	description="Getting started and troubleshooting MFA"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="brentserbus"
	ms.author="brserbus"
	displayOrder=""
	articleId="partner_center_mfa_secure_application_model"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32725796"
	clientIds='partnercenter'
	resourceTags="csp"
	productPesIds="17000"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>

# Getting started and troubleshooting MFA

Resource materials related to implementing partner security requirements immediately to safeguard your business. 

## **Recommended Steps**

This support topic area is for general questions around MFA for Partner center. If you have a specific question about configuration or transition from base line policy to security defaults, you should log these in the [Azure portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/supportRequest).

- [MFA is blocking me from supporting my customer with AOBO, what do I do?](https://docs.microsoft.com/partner-center/partner-security-requirements-faq#mfa-is-blocking-me-from-supporting-my-customer-using-aobo-what-should-i-do)
- [How do I confirm that my environment is complaint with the partner security requirements?](https://docs.microsoft.com/partner-center/partner-security-requirements#assessing-your-environment)
- [If I have already enabled MFA (through conditional access or any third party solution), how do I apply the required MFA for admins and end user protection baseline policies?](https://docs.microsoft.com/partner-center/partner-security-requirements-faq#is-it-a-requirement-to-enable-the-baseline-protection-policies)
- [Outlook isn't connecting after enabling MFA](https://docs.microsoft.com/partner-center/partner-security-requirements#do-you-have-users-using-office-365-provided-by-licenses-associated-with-your-partner-tenant)
- [Account lockouts happening while implementing MFA](https://docs.microsoft.com/partner-center/partner-security-requirements#configure-self-service-password-reset)
- [What should I know about security defaults?](https://docs.microsoft.com/partner-center/partner-security-requirements#security-defaults) 
- [How do I transition from Baseline policy to security defaults?](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults#enabling-security-defaults)
- Security defaults do not meet my needs, what [options](https://docs.microsoft.com/partner-center/partner-security-requirements#actions-that-you-need-to-take) can I consider? 
- I enabled Baseline policies, why has my MFA metric is suddenly dropped from 100%?

Effective February 29, 2020, Azure Active Directory (Azure AD) ["baseline" policies will be removed](https://docs.microsoft.com/azure/active-directory/fundamentals/whats-new#replacement-of-baseline-policies-with-security-defaults) and replaced with ["security defaults"](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), a more comprehensive set of protection policies for you and your customers. Security defaults in Azure AD can help protect your organization from common security attacks with preconfigured settings.

If you do not transition to security defaults before February 29, you will lose multi-factor authentication (MFA) enabled with baseline policies on your partner tenants. Please [enable security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults#enabling-security-defaults) as soon as possible to avoid any business disruptions. 

## **Recommended Documents**

* [Partner security requirements portal](https://partner.microsoft.com/resources/collection/partner-security-requirements)
* [Partner Security Requirements](https://docs.microsoft.com/partner-center/partner-security-requirements)
* [Partner Security Application Model Guide](https://assetsprod.microsoft.com/mpn/secure-application-model-guide.pdf)
* [Partner Security Requirements FAQ](https://docs.microsoft.com/partner-center/partner-security-requirements-faq)
* [Enabling the Secure Application Model framework](https://docs.microsoft.com/partner-center/develop/enable-secure-app-model)
* [CSP Partner Application Overview](https://assetsprod.microsoft.com/mpn/csp-partner-application-overview.pdf)
