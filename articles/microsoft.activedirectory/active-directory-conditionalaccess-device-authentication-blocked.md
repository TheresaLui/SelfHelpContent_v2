<properties
    pageTitle="Conditional Access - Policy blocked by device authentication"
    description="Conditional Access - Policy blocked by device authentication"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="zachoi"
    ms.author="zachoi"
    displayOrder="1"
    articleId="ISP_ConditionalAccess_DeviceAuthenticationBlocked"
	  diagnosticScenario="ConditionalAccess"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_ConditionalAccess"
/>

# Conditional Access Issue Preventing User Sign-In

<!--issueDescription-->

This is not an error – it is an intermediate event logged during sign-in indicating that device authentication is required due to a Conditional Access policy or because the application or resource requested the device ID in a token. Subsequent events in the sign-in logs may indicate whether device authentication was successful or not.

Device authentication may not be successful if the device is not compliant or if the device is not sending device state information to Azure AD. Note that device state information is not shared with Azure AD during authentication from an incognito browser or Chrome without the Windows 10 extension.

<!--/issueDescription-->

## **Recommended Documents**

- [Device registration overview](https://docs.microsoft.com/azure/active-directory/devices/overview)
- [Windows 10 Accounts](https://chrome.google.com/webstore/detail/windows-10-accounts/ppnbnpeolgkicgegkbkbjmhlideopiji)
- [Conditional Access Conditions](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-conditions)