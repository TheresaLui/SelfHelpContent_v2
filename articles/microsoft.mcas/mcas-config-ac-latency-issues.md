<properties
  pageTitle="I'm having issues around performance and latency with access and session controls"
  description="I'm having issues around performance and latency with access and session controls"
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
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues around performance and latency with access and session controls

Performance and latency issues may result for many reasons including factors outside of control Cloud App Security's proxy.

When investigating performance and latency issues, it's important to understand the specific scenarios, such as the following:

- I am experiencing a slow login
- My browser is experiencing latency
- My app is experiencing latency

Most users are able to resolve the issues using the steps below.

## **Recommended Steps**

- Investigate what other factors outside of the Cloud App Security proxy could be impacting the performance, such as:
  
  - Existing proxies/gateways/etc. that coexist with the Cloud App Security proxy
  - If applicable, remove any appliance in the environment that could be causing issues, such as proxy chaining
  - Location of where the user is coming from
  - Location of the targeted resource

**NOTE**:

- Functionality may differ between browsers. We recommend using one of the following fully-supported browsers: Microsoft Edge Chromium (latest), Google Chrome (latest), Mozilla Firefox (latest), Apple Safari (latest).
- We will continue to support the latest version of Internet Explorer and the legacy version of Microsoft Edge, but the support will be limited and we recommend using one of the fully-supported browsers

## **Recommended Documents**

- [Overview of Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad)
- [Session Controls](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad#how-session-control-works)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket with the following details:

- Which devices and/or browsers is this occurring on?
- The URL in which the error occurred
- Screenshots or recording showing the performance issue with and without the proxy
- Date, time, and user account that was used when the error occurred. These details can be retrieved from the Azure AD Sign-in Log
- A network trace of the performed action
