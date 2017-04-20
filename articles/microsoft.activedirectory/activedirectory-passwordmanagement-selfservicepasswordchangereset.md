<properties
    pageTitle="Password Management/Self-service password change/reset"
    description="Password Management/Self-service password change/reset"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045826"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# Password Management/Self-service password change/reset
## Prerequisites
* Ensure your tenant has a valid license to use Azure AD Self Service Password Reset:
	* Azure AD Premium 1
	* Azure AD Premium 2
	* Enterprise Mobility + Security E3
	* Enterprise Mobility + Security E5
	* Secure Productive Enterprise E3
	* Secure Productive Enterprise E5

## **Recommended steps**
1. Have your users register additional security info for self service password reset by directing them to [aka.ms/ssprsetup](https://login.microsoftonline.com/common/oauth2/authorize?client_id=0000000c-0000-0000-c000-000000000000&redirect_uri=https%3A%2F%2Faccount.activedirectory.windowsazure.com%2F&response_mode=form_post&response_type=code%20id_token&scope=openid%20profile&state=OpenIdConnect.AuthenticationProperties%3D02LGeV2aaOpBfeyrPlPTVE9v9W3rf0E_VtBiNcjuL12zhaz8BdJ613HFOdYPXhNva7OX8tUieWVS1ldrysmNHg-XCO7bW8Pe82sA4RnjWozG43QBmckgtxvqZvUaty0ZNhBtzMtrjG5qW1v06t4jCAd03c-h0opfkRABw4Y2cvKoYnQy0tfpyRsC1KI3DngNKzhbtPXIYKjxHw02Ld-9RgJVjNxRrMppzhE6EJsjbfD0PpnwbwLp-tMnT5M3hS60SJwZQjvjfocM-x2EcXJhPhG1lfbSGIoZi3yHh12qyVI&nonce=1491428196.4kvRPWtSmTOR_qzakP8WpQ&nux=1).
	* You can also pre-populate data (email and phone attributes) for your users using an API, Powershell, or Azure AD Connect.
	* To learn how read:
		* [Deploying password reset without requiring users to register](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
		* [What data is used by password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)
2. After data is populated for the user (by the user themselves or the administrator) direct them to [aka.ms/sspr](https://passwordreset.microsoftonline.com/) so your users can be empowered to reset their own passwords.
3. If users are still experiencing problems they are most likely **federated** or **password hash synched** users. This means there is likely a problem with the Password Writeback service.
	* For quick writeback fixes check [Tip 5](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-5-writeback---look-at-the-application-event-log-on-your-aad-connect-machine-to-troubleshoot-password-writeback) and [Tip 6](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-6-writeback---ensure-you-enable-the-correct-permissions-firewall-rules-and-connection-settings-for-password-writeback) from our [Top Tips](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
	* For more information on Password Writeback configuration read:
		* [How to enable users to reset their Azure AD passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
		* [How to enable users to reset or change their on-premises Active Directory passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-or-change-their-ad-passwords)


## **Recommended documents**
* [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [FAQ - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset)
* [FAQ - Password Reset Registration](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset-registration)
* [FAQ - Password Change](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-change)
* [Troubleshoot - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [Troubleshoot - Password Reset Registration](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-registration-portal)
* [How to update your own password](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-update-your-own-password)
* [Getting Started with Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [Best Practices - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)
