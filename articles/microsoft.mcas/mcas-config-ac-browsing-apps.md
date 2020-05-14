<properties
  pageTitle="I’m having issues with session controls while browsing a protected application"
  description="I’m having issues with session controls while browsing a protected application"
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
  cloudEnvironments="public"
/>

# I’m having issues with session controls while browsing a protected application

Browsing a protected application that has been secured using session controls allows a user to access a web-based application while restricting actions such as copy, cut, paste, download, upload, and some custom activities. You can verify that session controls are enforced when you see `*.cas.ms` appended to the URL.

Most users are able to resolve the following issues using the steps below:

- Blocking an action is not enforced
- My application is missing functionality or is unresponsive

## **Recommended Steps**

- Make sure you are using sessions controls with a web-based app

    > [!NOTE]
    > Session controls can only be enforced on web-based applications. Access controls can be enforced on native applications.
- In your Azure Active Directory Conditional Access policy, under **Sessions**, clear **Conditional Access App Control**. If the issue persists, open a ticket for the relevant application.
- If you are using a Cloud App Security session policy, in your Azure AD Conditional Access policy, under **Sessions**, make sure that **Use Custom Policy** is selected.

## **Recommended Documents**

- [Overview of Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad)
- [Session Controls](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad#how-session-control-works)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket with the following details:

- Which devices and/or browsers is this occurring on?
- The URL in which the error occurred
- Screenshots or recording showing the issue
- Date, time, and user account that was used when the error occurred. These details can be retrieved from the Azure AD Sign-in Log
- A network trace of the performed action
