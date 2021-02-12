<properties
    pageTitle="I'm having a problem with password writeback"
    description="Password reset/Password Writeback"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia"
    ms.author="zhchia"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565598,32629794"
    resourceTags=""
    productPesIds="16579,16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="87cc194f-57ea-49bc-a135-941b17ad4c4b"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# I'm having a problem with password writeback

## **Recommended Steps**

**I'm having problems configuring password writeback**

* Password writeback is a premium feature
* Make sure you that you understand the licensing requirements:

  * You must have at least one license assigned in your organization
   * **Cloud only users** - Any Office 365 (O365) paid SKU, or Azure AD Basic
   * **Cloud and/or on-premises users** - Azure AD Premium P1 or P2, Enterprise Mobility + Security (EMS), or Secure Productive Enterprise (SPE)
    * To read more about licensing requirements see the article [Licensing requirements for Azure AD self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)

* You have at least one administrator account and one test user account with one of the appropriate license
* You must connect Azure AD Connect to the Primary Domain Controller Emulator for password writeback to work. You can configure Azure AD Connect to use a Primary Domain Controller by right clicking on the **properties** of the Active Directory synchronization connector, then selecting **configure directory partitions**. From there, look for the **domain controller connection settings** section and check the box titled **only use preferred domain controllers**. Note: If the preferred DC is not a PDC emulator, Azure AD Connect will still reach out to the PDC for password writeback.
* Password reset has been configured and enabled in your tenant. For more information, see [Enable users to reset their Azure AD passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords).
* Make sure that the administrator account being used to enable Password Writeback is a cloud administrator account (created in Azure AD not on-premises AD)
* You have a single or multi-forest AD on-premises deployment running Windows Server 2008 R2, Windows Server 2012, or Windows Server 2012 R2 with the latest service packs installed
* You have the Azure AD Connect tool installed and you have prepared your AD environment for synchronization to the cloud. *Before testing password writeback, make sure that you first complete a full import and full sync from both AD and Azure AD in Azure AD Connect*.
 * Read more on how to do a [full sync and full import in Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations#staging-mode)

**I'm having a problem with password writeback connectivity**

1. Download and enable the latest version of [Azure AD Connect](https://www.microsoft.com/download/details.aspx?id=47594)
2. Firewall configuration: The Azure AD Connect tool (1.1.443 and above) will need **outbound HTTPS** access to:

    * passwordreset.microsoftonline.com
    * servicebus.windows.networks
    
3. Allow idle connections to persist for at least 2-3 minutes

**I'm still having problems with password writeback**

* If you are still having difficulty, try disabling and re-enabling the password writeback service in the Azure AD Connect tool
* Read more on how to [disable and re-enable password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#disable-and-re-enable-the-password-writeback-feature)

## **Recommended Documents**

* [Troubleshoot Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [Password Writeback Event Log Error Codes](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [Troubleshoot Password Writeback Connectivity](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [FAQ - Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)
