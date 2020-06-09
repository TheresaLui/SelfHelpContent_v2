<properties
    pageTitle="I don't think I have the correct permissions, firewall rules, or connection settings for password writeback"
    description="Top Tips from customers - Tip 6"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="600"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="da73114e-feeb-4a44-9d7d-2bbaac131c50"
	ownershipId="AzureIdentity_User"
/>
# I don't think I have the correct permissions, firewall rules, or connection settings for password writeback

## **Recommended steps**
In order for writeback to work correctly, you must ensure:

1. The proper **Active Directory permissions** have been set for users using the password writeback feature such that they have rights to modify their own passwords and account unlock flags in AD
2. The proper **firewall ports** have been opened to allow the password writeback service to communicate securely with the outside world using an outbound connection
3. The proper **firewall exceptions** have been made for key password reset service URLs, such as Service Bus
4. Your **proxy and firewall are not killing idle outbound connections**, we recommend 10 minutes or longer

For a full list of troubleshooting guidance and specific guidelines for configuring permissions and firewall rules for password writeback go [here](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords):






[view on DOCS.com](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-6-writeback---ensure-you-enable-the-correct-permissions-firewall-rules-and-connection-settings-for-password-writeback)

## **Recommended documents**
* [Troubleshoot - Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [Password Writeback event log error codes](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [Troubleshoot - Password Writeback connectivity](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [Writeback deployment - Step 3: Configure your firewall](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#step-3-configure-your-firewall)
* [Writeback deployment - Step 4: Set up the appropriate permissions](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#step-4-set-up-the-appropriate-active-directory-permissions)
* [FAQ - Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)
