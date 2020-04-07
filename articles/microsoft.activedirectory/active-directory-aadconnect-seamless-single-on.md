<properties
  pageTitle="Problems configuring and signing in with Azure AD Seamless Single Sign-on"
  description="Problems configuring and signing in with Azure AD Seamless Single Sign-on"
  service="microsoft.aad"
  resource="Microsoft_AAD_IAM"
  authors="billmath"
  ms.author="billmath"
  displayOrder=""
  selfHelpType="generic"
  supportTopicIds="32596867,32629770"
  resourceTags="aadconnect,aadconnect_seamless_single_sign_on,managed_authentication"
  productPesIds="16579,16666"
  cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
  articleId="c300cc33-1cc1-4136-a957-b36423c13730"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Problems configuring and signing in with Azure AD Seamless Single Sign-on

## **Recommended Steps**

1. If you are configuring Seamless Single Sign-on for the first time, please ensure that you have reviewed the [Introduction](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso), [quick start](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start), and [FAQ](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-faq). Please note that Seamless SSO works with Password Hash Synchronization and Pass-through Authentication, but not with AD FS.
2. Review [known issues](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sso#known-problems) of Seamless SSO
3. If you are experiencing single sign-on issues from an [Azure AD-joined device](https://docs.microsoft.com/azure/active-directory/device-management-introduction) instead of a domain-joined device, follow the troubleshooting guides under the **Devices** *problem type*. Learn more [here](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-faq#what-is-the-difference-between-the-single-sign-on-experience-provided-by-azure-ad-joinactive-directory-azureadjoin-overviewmd-and-seamless-sso).
4. If you don't experience single sign-on and need to enter your username (but no password) instead, it is likely that the app you are signing into isn't forwarding the **domain_hint** or **whr** or **login_hint** parameter to Azure AD. [Here](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-faq#what-applications-take-advantage-of-domainhint-or-loginhint-parameter-capability-of-seamless-sso) is a list of apps that take advantage of these parameters.
5. If you have already configured Seamless SSO, ensure that you roll over its keys every 30 days. Learn more [here](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-faq#how-can-i-roll-over-the-kerberos-decryption-key-of-the-azureadssoacc-computer-account).
6. If you want to make a feature request, use our [UserVoice forum](https://feedback.azure.com/forums/169401-azure-active-directory/category/160611-directory-synchronization-aad-connect)

## **Recommended Documents**

  * [Troubleshooting checklist](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sso#troubleshooting-checklist)
  * [Re-configuring Seamless SSO using PowerShell](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sso#manual-reset-of-the-feature)
  * [Registering non-Windows 10 devices without AD FS](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-faq#i-want-to-register-non-windows-10-devices-with-azure-ad-without-using-ad-fs-can-i-use-seamless-sso-instead)
  * [Rolling over Seamless SSO keys](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-faq#how-can-i-roll-over-the-kerberos-decryption-key-of-the-azureadssoacc-computer-account)
  * [Disabling Seamless SSO](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-faq#how-can-i-disable-seamless-sso)
