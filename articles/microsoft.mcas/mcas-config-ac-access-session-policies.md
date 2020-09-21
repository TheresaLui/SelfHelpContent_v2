<properties
  pageTitle="I'm having issues with access and session policies"
  description="I'm having issues with access and session policies"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-config-ac-access-session-policies"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32745217"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_CAAC"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues with access and session policies

Access and Session policies in Cloud App Security allow you to configure adaptive controls that are enforced in real time.

Most users are able to resolve the following issues using the steps below:

- I'm getting an error when trying to create policies
- My access or session policy is not enforced as expected

## **Recommended Steps**

1. If you are using Azure Active Directory, in the Active Directory portal, in the relevant Conditional Access policy, under **Session**, make sure that **Use Conditional Access App Control** is selected.

    * If you are not using a custom Cloud App Security policy, in the dropdown select **Monitor Only** or **Block Downloads**
    * Otherwise, in the dropdown select **Use Custom Policy** and in Cloud App Security, create granular access or session control policies, such as block upload, copy/paste/print, or block downloads based on content inspection

1. If you are using a third-party Identity provider, make sure to onboard the app first. In Cloud App Security, browse to **Investigate** > **Connected apps** > **Conditional Access App Control apps**, and click the plus sign to start the process.

1. If you are trying to create a session policy and see a "no apps onboarded" error message, verify that the app appears on the **Conditional Access App Control apps** page. If the app does not appear, log in to app. If the app still does not appear, please continue with opening the ticket.

## **Recommended Documents**

- [Overview of Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-intro-aad)
- [Access policies](https://docs.microsoft.com/cloud-app-security/access-policy-aad)
- [Session policies](https://docs.microsoft.com/cloud-app-security/session-policy-aad)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
