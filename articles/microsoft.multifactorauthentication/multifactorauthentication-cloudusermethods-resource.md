<properties
  pageTitle="Cloud-based MFA/User MFA methods issues (cloud)"
  description="User MFA methods issues"
  service="microsoft.aad"
  resource="Microsoft_AAD_IAM"
  authors="kgremban"
  displayOrder="120"
  selfHelpType="resource"
  supportTopicIds=""
  resourceTags="mfa_overview"
  productPesIds=""
  cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b1048d87-19b4-4c0b-b99b-254dbd2c27cb"
	ownershipId="AzureIdentity_User"
/>

# Troubleshoot your users' authentication issues

## **Recommended steps**

### Text messages never arrive or are significantly delayed 

Issues with text messages are usually a result of phone reception and signal strength, the handling of tone dials by the local PBX and phone network, interferences on the line, background noises on the call, technical faults with an individual device, and other similar causes external to the MFA server. If your users often have problems with reliably receiving text messages, tell them to use the mobile app verification method instead.

### What can I do to ensure users who don’t have access to their phones are able to sign in? 

Ensure that your users configured more than one verification method, such as an office phone. Tell them to try signing in again, but select a different verification method on the sign-in page.

## **Recommended documents**

- [Managing user settings with Azure Multi-Factor Authentication in the cloud](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-manage-users-and-devices)  
- [Manage and support user accounts](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-faq#manage-and-support-user-accounts) 