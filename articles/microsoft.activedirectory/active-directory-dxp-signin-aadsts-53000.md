<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-53000"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# How Do I Resolve the User Sign-in Issues?

<!--issueDescription-->
Based on the information you provided we have identified following issue and recommend taking the action to resolve the issue.

**Error Code:** 53000

**Message:** Device is not in required device state: {state}. Conditional Access policy requires a compliant device, and the device is not compliant. The user must enroll their device with an approved MDM provider like Intune.
<!--/issueDescription-->

**Action:** The device did not send the required device registration information to Azure AD during sign-in. This can happen if the device is not managed and compliant or if the device is managed and compliant but the application did not send the device compliance information to Azure AD. <br><br>To resolve this issue: <br>1. Review the device configuration in Azure AD to see if the device is managed or not <br>2. Review the device compliance in Intune or other MDM. If the device is compliant, the device ID should appear in the sign-in logs <br>3. If the device is compliant and managed, the application may not be sending the device compliance information to Azure AD. This can happen if the sign-in is using an inPrivate browser, a Chrome browser without the Windows 10 extension, or if the client application doesn't support modern authentication. <br><br>You can refer to the following links for the steps to resolve the issue.

<ul><li> <a href='https://docs.microsoft.com/azure/active-directory/devices/overview'>What is a device identity?</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/devices/concept-primary-refresh-token'>What is a Primary Refresh Token?</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-compliant-device'>How to create a Conditional Access policy to require compliance devices?</a></li></ul>
