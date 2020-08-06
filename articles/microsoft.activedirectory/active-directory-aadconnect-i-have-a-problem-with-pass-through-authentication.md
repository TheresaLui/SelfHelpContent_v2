<properties
  pageTitle="I have a problem with Azure AD Pass-through Authentication"
  description="I have a problem with Azure AD Pass-through Authentication"
  service="microsoft.aad"
  resource="Microsoft_AAD_IAM"
  authors="rodejo"
  ms.author="rodejo"
  displayOrder=""
  selfHelpType="generic"
  supportTopicIds="32684515"
  resourceTags="aadconnect,aadconnect_pass_through_authentication,managed_authentication"
  productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
  articleId="c6546fa2-9f7b-4f75-b3d5-985156272dc2"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# I have a problem with Azure AD Pass-through Authentication

## **Recommended Steps**

1. Before making any changes to your Pass-through Authentication configuration, [add a cloud-only Global Administrator account to your tenant.](https://docs.microsoft.com/azure/active-directory/add-users-azure-active-directory)  This step ensures that you don't get locked out of your tenant if you make a configuration mistake.
2. If you want to make a request for a change please use our [UserVoice forum!](https://feedback.azure.com/forums/169401-azure-active-directory/category/160611-directory-synchronization-aad-connect)

### Troubleshooting configuration of Pass-through Authentication

  * [Issues with enabling Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-pass-through-authentication#issues-with-enabling-the-feature)
  * [Issues with enabling Exchange ActiveSync support](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-pass-through-authentication#exchange-activesync-configuration-issues)
  * [Disabling Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-faq#how-can-i-disable-pass-through-authentication)

### Troubleshooting Authentication Agent-related issues

  * [Issues related to installing Authentication Agents](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-pass-through-authentication#authentication-agent-installation-issues)
  * [Issues related to registering Authentication Agents](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-pass-through-authentication#authentication-agent-registration-issues)
  * [Issues related to uninstalling Authentication Agents](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-pass-through-authentication#authentication-agent-uninstallation-issues)
  * [Upgrading preview Authentication Agents](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-upgrade-preview-authentication-agents)

### Troubleshooting user sign-in issues

  * [General sign-in issues](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-pass-through-authentication#general-issues)
  * [Debugging user sign-in issues](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-pass-through-authentication#collecting-pass-through-authentication-agent-logs)
  * [Issues with lockout of users' on-premises Active Directory accounts](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-smart-lockout)

## **Recommended Documents**

* [I have a problem installing, registering or uninstalling Authentication Agents](#troubleshooting-authentication-agent-related-issues)
* [I have a problem with users signing in using Pass-through Authentication](troubleshooting-user-sign-in-issues)
* [I have a problem enabling or disabling Pass-through authentication or enabling Exchange ActiveSync](#troubleshooting-configuration-of-pass-through-authentication)
*  [I want to learn how I can configure Azure AD Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication)
* [I have a question about Azure AD Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-faq)
 * [I want to learn about the current limitations of Azure AD Pass-through Authentication are](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-current-limitations) 
 * [I have a security-related question about Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-security-deep-dive)
 * [I want to learn how to migrate from AD FS to Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-faq#i-already-use-ad-fs-to-sign-in-to-azure-ad-how-do-i-switch-it-to-pass-through-authentication)
* [I want to configure Pass-through Authentication for high availability](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-quick-start#step-5-ensure-high-availability)
