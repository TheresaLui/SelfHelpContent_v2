<properties
  pageTitle="I'm having a problem with configuring access controls for native apps"
  description="I'm having a problem with configuring access controls for native apps"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-config-ac-native-apps"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728962"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_CAAC"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having a problem with configuring access controls for native apps

Access controls can be used to monitor or block access to a native app. Session controls are only supported for web-based apps.

Most users are able to resolve the following issues using the steps below:

- I am not able to login to my native app
- My native app is not recognized
- I cannot configure controls for my native app

## **Recommended Steps**

- Make sure that you are enforcing access controls and not session controls

    **NOTE**  
    Access controls can be enforced on native apps. Session controls can only be enforced on web-based apps.
- If you are unable to block access to your native app, in your access policy, set the **Client app filter** to **Mobile** and **Desktop**. If this is not set, the resulting policy will only apply to browser sessions.
- Validate your sign in flow by downloading the Azure AD sign-in logs in the JSON file format. If you proceed to open the support case, make sure you include the file with the ticket.

    **NOTE**  
    The Authenticator app, among other native client app sign-in flows, uses a non-interactive sign-in flow and cannot be used with access controls.

## **Recommended Documents**

- [Overview of Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad)
- [Supported Apps and Clients](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad#supported-apps-and-clients)
- [Access policies](https://docs.microsoft.com/cloud-app-security/access-policy-aad)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
