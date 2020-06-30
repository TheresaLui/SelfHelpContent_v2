<properties
    pageTitle="I have a problem with password writeback"
    description="I have a problem with password writeback"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32684517"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="3b956452-6faf-4b11-babc-c2bb0669d9fa"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# I have a problem with Password Writeback

## **Recommended Steps**

* [I'm having a problem with password writeback connectivity](#i'm-having-a-problem-with-password-writeback-connectivity)
* [Password Writeback is not working at all](#password-writeback-is-not-working-at-all)
* [Password Writeback used to work but now it stopped working](#password-writeback-stopped-working)
* [I enabled Password Writeback but it is not working. What are the licensing requirements?](#what-are-the-licensing-requirements-for-password-writeback?")
* [I get an error message when using Password Writeback](#password-writeback-event-log-error-codes)
* [I have a question about Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)

### Password Writeback is not working at all

If you are enabling Password Writeback for your tenant but it is not working, please verify the following:

* Make sure Password Reset has been configured and enabled in your tenant. For more information, see [Enable users to reset their Azure AD passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords).
* Make sure that the administrator account being used to enable Password Writeback is a **cloud administrator account** (created in Azure AD not on-premises AD)
* Verify that you have a single or multi-forest AD on-premises deployment running **Windows Server 2008 R2, Windows Server 2012, or Windows Server 2012 R2 with the latest service packs installed**
* You have the Azure AD Connect tool installed and you have prepared your AD environment for synchronization to the cloud. *Before testing password writeback, make sure that you **first complete a full import and full sync** from both AD and Azure AD in Azure AD Connect*.
  * Read more on how to do a [full sync and full import in Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations#staging-mode)

## I'm having a problem with password writeback connectivity

1. Verify the firewall configuration: Azure AD Connect (1.1.443 and above) will need **outbound HTTPS** access to:

    * passwordreset.microsoftonline.com
    * servicebus.windows.networks
    
2. Allow idle connections to persist for at least 2-3 minutes

### Password Writeback stopped working

* Try disabling and re-enabling the password writeback service in Azure AD Connect
Read more on how to [disable and re-enable password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#disable-and-re-enable-the-password-writeback-feature)

### Password Writeback Event Log error codes

* [Review the Windows Applications Event log for any error events](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes) that are related to Password Writeback

### What are the licensing requirements for Password Writeback?

Password Writeback is an Azure AD premium feature, which means that your users need to have an Azure AD license assigned to them. These are the licensing requirements for Password Writeback:

* You must have at least one license assigned in your organization:
  
    * **Cloud only users** - Any Office 365 (O365) paid SKU, or Azure AD Basic
    * **Cloud and/or on-premises users** - Azure AD Premium P1 or P2, Enterprise Mobility + Security (EMS), or Secure Productive Enterprise (SPE)
    * You have at least one administrator account and one test user account with one of the appropriate license

To read more about licensing requirements see the article [Licensing requirements for Azure AD self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)

## **Recommended Documents**

* [Troubleshoot Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [Password Writeback Event Log Error Codes](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [Troubleshoot Password Writeback Connectivity](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [FAQ - Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)
