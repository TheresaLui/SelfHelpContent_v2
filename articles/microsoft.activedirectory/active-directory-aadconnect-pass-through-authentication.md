<properties
  pageTitle="Problems configuring and signing in with Azure AD Pass-through Authentication"
  description="Problems configuring and signing in with Azure AD Pass-through Authentication"
  service="microsoft.aad"
  resource="Microsoft_AAD_IAM"
  authors="billmath"
  ms.author="billmath"
  displayOrder=""
  selfHelpType="generic"
  supportTopicIds="32596862,32629769"
  resourceTags="aadconnect,aadconnect_pass_through_authentication,managed_authentication"
  productPesIds="16579,16666"
  cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
  articleId="5e0305b5-a7a4-43d7-bd00-aa3bf679ca91"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Problems configuring and signing in with Azure AD Pass-through Authentication

## **Recommended Steps**

1. If you are configuring Pass-through Authentication for the first time, please ensure that you have reviewed the [Introduction](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication), [quick start](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-quick-start), and [FAQ](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-faq) articles
2. Review [current limitations](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-current-limitations) of Pass-through Authentication to ensure that you are not experiencing a known issue. As a workaround to such issues, enable Password Hash Synchronization on the [Optional features](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom#optional-features) page in the Azure AD Connect wizard.
3. If you have security-related questions about Pass-through Authentication, read this [article](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-security-deep-dive).
4. If you are planning to migrate from AD FS to Pass-through Authentication, review this [article](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-user-signin) for comparison between the sign-in methods, and review this [FAQ entry](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-faq#i-already-use-ad-fs-to-sign-in-to-azure-ad-how-do-i-switch-it-to-pass-through-authentication) for more details on how to do the migration
5. Before making any changes to your Pass-through Authentication configuration, add a cloud-only Global Administrator account to your tenant. Learn more [here](https://docs.microsoft.com/azure/active-directory/add-users-azure-active-directory) on how to do so. This step ensures that you don't get locked out of your tenant.
6. If you have already configured Pass-through Authentication, please configure your tenant for [high availability](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication-quick-start#step-5-ensure-high-availability)
7. If you want to make a feature request, use our [UserVoice forum](https://feedback.azure.com/forums/169401-azure-active-directory/category/160611-directory-synchronization-aad-connect)

## **Recommended Documents**

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
