<properties
  pageTitle="I’m having issues around performance and latency with access and session controls"
  description="I’m having issues around performance and latency with access and session controls"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-config-ac-latency-issues"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728983"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_CAAC"
  cloudEnvironments="public"
/>

# I’m having issues around performance and latency with access and session controls

Performance and latency issues may result from many factors outside of Cloud App Security's proxy. In general, all proxies add latency including the Cloud App Security proxy.

When investigating performance and latency issues, it’s important to understand the specific scenarios, such as the following:

- I am experiencing a slow login
- My browser is experiencing latency
- My application is experiencing latency

Most users are able to resolve the issues using the steps below.

## **Recommended Steps**

- Investigate what other factors outside of the Cloud App Security proxy could be impacting the performance, such as:
  - Existing proxies/gateways/etc. that coexist with the Cloud App Security proxy
    - If applicable, remove any appliance in the environment that could be causing issues, such as proxy chaining
  - Location of where the user is coming from
  - Location of the targeted resource
- If you are not using one of the fully-supported browsers, switch to one of them and try again.
- If you are not using the latest version of a supported browser, upgrade to the latest version and try again.

    > [!NOTE]
    >
    > - Functionality may differ between browsers. We recommend using one of the following fully-supported browsers:<br />- Microsoft Edge Chromium (latest)<br />- Google Chrome (latest)<br />- Mozilla Firefox (latest)<br />- Apple Safari (latest)
    > - We will continue to support the latest version of Internet Explorer and the legacy version of Microsoft Edge, but the support will be limited and we recommend using one of the fully-supported browsers.

## **Recommended Documents**

- [Overview of Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-intro-aad)
- [Session Controls](https://docs.microsoft.com/en-us/cloud-app-security/proxy-intro-aad#how-session-control-works)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket with the following details:

- Which devices and/or browsers is this occurring on?
- The URL in which the error occurred
- Screenshots or recording showing the issue
- Date, time, and user account that was used when the error occurred. These details can be retrieved from the Azure AD Sign-in Log
- A network trace of the performed action
