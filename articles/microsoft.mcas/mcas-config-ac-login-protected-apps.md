<properties
  pageTitle="I’m having issues with access controls when logging into my protected app"
  description="I’m having issues with access controls when logging into my protected app"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-config-ac-login-protected-apps"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728988"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_CAAC"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I’m having issues with access controls when logging into my protected app

When logging into a protected app, access controls are enforced. Access controls allow or block access to the app based on conditions, such as the device type, app type, or location that can be configured in the access policy.

Most users are able to resolve the following issues using the steps below:

- I am experiencing a slow login
- I get stuck in a loop when trying to log in
- The app displays a failure message when I try to log in

## **Recommended Steps**

- Verify that access controls are enforced by checking that `*.access-control.cas.ms` is appended to the URL. If the suffix is missing, check the [access policy settings](https://docs.microsoft.com/cloud-app-security/access-policy-aad).

- Make sure you are using sessions controls with a web-based app

**NOTE**:  Session controls can only be enforced on web-based apps. Access controls can be enforced on native apps.

- Validate your sign-in flow by downloading the Azure Active Directory (Azure AD) sign-in logs in the JSON file format. If you proceed to open the support case, make sure you include the file with the ticket.

**NOTE**: The Authenticator app, among other native client app sign-in flows, uses a non-interactive sign-in flow and cannot be used with access controls.

- If you are using a custom app, and the app is stuck in a loop trying to log in, try changing the settings for nonce handling:

    * In Cloud App Security, browse to **Investigate** > **Connected apps** > **Conditional Access App Control**
    * In the list of apps, on the row in which the app you are deploying appears, choose the three dots at the end of the row, and then under **APP DETAILS**, choose **Edit**
    * Change the nonce-handling settings and then click **Save**

- In Azure AD, go to the relevant conditional access policy, and clear **Use Conditional Access App Control**. If the issue is still not resolved, open a ticket for Azure AD.
- If the app displays a failure message when you try to log in, make a note of the displayed **request id**, and then restart your browser session. If the issue persists, please continue with opening the ticket and include the **request id** in the details.

## **Recommended Documents**

- [Overview of Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad)
- [Access Controls](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad#access-controls)
- [Access policies](https://docs.microsoft.com/cloud-app-security/access-policy-aad)
- [Any app deployment](https://docs.microsoft.com/cloud-app-security/proxy-deployment-any-app)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
