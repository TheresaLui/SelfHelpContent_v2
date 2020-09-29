<properties
    pageTitle="Problems with A"
    description="Top Tips from customers - Tip 5"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="500"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="8e239995-834a-4f64-afbb-d1c82b40d1ca"
	ownershipId="AzureIdentity_User"
/>
# I want to look at an event log to troubleshoot password writeback

## **Recommended steps**
You can look at the Azure AD Connect Application Event log to troubleshoot password writeback. It contains a rich set of logging information that describes much of what is occuring with the password writeback service, in real time. To get access to this log, follow the steps below:

1. Sign in to on-premises computer that is running **Azure AD Connect**.
2. Open the **Windows Event Viewer** by pressing **Start** and typing in **"Event Viewer"**.
3. Open the **Application** event log.
4. Look for events from the following sources: **PasswordResetService** or **ADSync** to learn more about what issue may be occuring.

For a full list of events that can appear in this log, as well as a bunch more troubleshooting guidance for password writeback, see **Recommended documents**:

[view on DOCS.com](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-5-writeback---look-at-the-application-event-log-on-your-aad-connect-machine-to-troubleshoot-password-writeback)

## **Recommended documents**
* [Troubleshoot - Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [Password Writeback event log error codes](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [Troubleshoot - Password Writeback connectivity](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [Writeback deployment - Step 3: Configure your firewall](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#step-3-configure-your-firewall)
* [Writeback deployment - Step 4: Set up the appropriate permissions](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#step-4-set-up-the-appropriate-active-directory-permissions)
* [FAQ - Password Writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)
