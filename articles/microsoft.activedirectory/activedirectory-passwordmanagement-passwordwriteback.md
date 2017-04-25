<properties
    pageTitle="I'm having a problem with password writeback"
    description="Password Management/Password Writeback"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia, gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565598"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# I'm having a problem with password writeback
## **Recommended steps**
* Ensure your tenant has a valid license to use Azure AD Self Service Password Reset:
	* Azure AD Premium 1
	* Azure AD Premium 2
	* Enterprise Mobility + Security E3
	* Enterprise Mobility + Security E5
	* Secure Productive Enterprise E3
	* Secure Productive Enterprise E5
  
  The last word on Azure AD licensing (and always the most-recently-updated source) is the [Azure Active Directory Pricing page](https://azure.microsoft.com/pricing/details/active-directory/).

* You have at least one administrator account and one test user account with one of the aforementioned licenses.

* You must connect Azure AD Connect to the Primary Domain Controller Emulator for password writeback to work. If you need to, you can configure Azure AD Connect to use a Primary Domain Controller by right clicking on the **properties** of the Active Directory synchronization connector, then selecting **configure directory partitions**. From there, look for the **domain controller connection settings** section and check the box titled **only use preferred domain controllers**. *Note: If the preferred DC is not a PDC emulator, Azure AD Connect will still reach out to the PDC for password writeback.*

* Password reset has been configured and enabled in your tenant. For more information, see [Enable users to reset their Azure AD passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords).

* Make sure that the administrator account being used to enable Password Writeback is a cloud administrator account (created in Azure AD not on-prem AD)

* You have a single or multi-forest AD on-premises deployment running Windows Server 2008 R2, Windows Server 2012, or Windows Server 2012 R2 with the latest service packs installed.

* You have the Azure AD Connect tool installed and you have prepared your AD environment for synchronization to the cloud. *Before testing password writeback, make sure that you first complete a full import and full sync from both AD and Azure AD in Azure AD Connect*.

## **Recommended steps**
1. Download the latest version of Azure AD Connect [1.1.443.0](https://www.microsoft.com/download/details.aspx?id=47594)
2. Enable password Writeback in Azure AD Connect
3. Configure your firewall
	* The Azure AD Connect tool (1.1.443 and above) will need **outbound HTTPS** access to:
		* passwordreset.microsoftonline.com
		* servicebus.windows.networks
4. Allow idle connections to persist for at least 2-3 minutes.

If you are still having difficulty, try disabling and re-enabling the service in the Azure AD Connect tool.


## **Recommended documents**
* [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [Troubleshoot Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [Password Writeback Event Log Error Codes](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [Troubleshoot Password Writeback Connectivity](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [FAQ - Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)
