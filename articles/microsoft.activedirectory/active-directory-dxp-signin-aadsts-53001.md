<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-53001"
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

**Error Code:** 53001

**Message:** Device is not in required device state: {state}. Conditional Access policy requires a Hybrid Azure AD joined device, and the device is not Hybrid Azure AD joined or the sign-in does attempt did not provide the required device information.
<!--/issueDescription-->

**Action:** The device did not send the required device registration information to Azure AD during sign-in. This can happen if the device is not hybrid joined to the Azure AD domain or the device is hybrid joined but the application being used had a problem accessing the device join information. This can happen if the sign-in occurs using an inPrivate browser, a Chrome browser without the Windows 10 extension, or if the client application doesn't support modern authentication. <br><br>You can refer to the following links for the steps to resolve the issue.

<ul><li>You can view additional information in the <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/SignInEventsV3Blade/{key}/{value}/'>Sign-in Logs</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access'>Troubleshooting sign-in problems with Conditional Access</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/devices/concept-primary-refresh-token'>What is a Primary Refresh Token?</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/devices/troubleshoot-hybrid-join-windows-current'>Troubleshooting hybrid Azure Active Directory joined devices</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join'>Azure AD joined devices</a></li></ul>
