<properties
    pageTitle="Problems with A"
    description="Top Tips from customers - Tip 5"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    ms.author="gahug"
    displayOrder="20"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="MoonCake"
 	articleId="activedirectory-passwordmanagement-troubleshoot-4-mooncake"
	ownershipId="AzureIdentity_User"
/>
# I want to look at an event log to troubleshoot password writeback

## **Recommended Steps**

You can look at the Azure AD Connect Application Event log to troubleshoot password writeback. It contains a rich set of logging information that describes much of what is occurring with the password writeback service, in real time. To get access to this log, follow the steps below:

1. Sign in to on-premises computer that is running **Azure AD Connect**.
2. Open the **Windows Event Viewer** by pressing **Start** and typing in **"Event Viewer"**.
3. Open the **Application** event log.
4. Look for events from the following sources: **PasswordResetService** or **ADSync** to learn more about what issue may be occurring.