<properties
  pageTitle="I'm having issues with session controls while browsing a protected app"
  description="I'm having issues with session controls while browsing a protected app"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-config-ac-browsing-apps"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728966"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_CAAC"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues with session controls while browsing a protected app

Browsing a protected app that has been secured using session controls allows a user to access a web-based app while restricting actions such as copy, cut, paste, download, upload, and some custom activities.

Most users are able to resolve the following issues using the steps below:

- Blocking an action is not enforced
- My app is missing functionality or is unresponsive

## **Recommended Steps**

- Verify that session controls are enforced by checking that `*.cas.ms` is appended to the URL
- Make sure you are using sessions controls with a web-based app

 **NOTE**: Session controls can only be enforced on web-based apps. Access controls can be enforced on native apps.
 
- In your Azure Active Directory Conditional Access policy, under **Sessions**, clear **Conditional Access App Control**. If the issue persists, open a ticket for the relevant app.
- If you are using a Cloud App Security session policy, in your Azure AD Conditional Access policy, under **Sessions**, make sure that **Use Custom Policy** is selected

## **Recommended Documents**

- [Overview of Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad)
- [Session Controls](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad#how-session-control-works)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket with the following details:

- Which devices and/or browsers is this occurring on?
- The URL in which the error occurred
- Screenshots or recording showing the issue
- Date, time, and user account that was used when the error occurred. These details can be retrieved from the Azure AD Sign-in Log.
- A network trace of the performed action
