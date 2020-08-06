<properties
    pageTitle="Cloud-based MFA/User MFA methods issues (cloud)"
    description="User MFA methods issues"
    service="microsoft.multifactorauthentication"
    resource=""
    authors="kgremban"
    selfHelpType="generic"
    supportTopicIds="32570992"
    productPesIds="14947,16579"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    	articleId="6b261f05-a624-4416-870e-4701bede999a"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# User MFA methods issues

## **Recommended steps**

### Text messages never arrive or are significantly delayed 

Issues with text messages are usually a result of phone reception and signal strength, the handling of tone dials by the local PBX and phone network, interferences on the line, background noises on the call, technical faults with an individual device, and other similar causes external to the MFA server. If your users often have problems with reliably receiving text messages, tell them to use the mobile app verification method instead.

### What can I do to ensure users who don’t have access to their phones are able to sign in? 

Ensure that your users configured more than one verification method, such as an office phone. Tell them to try signing in again, but select a different verification method on the sign-in page.

## **Recommended documents**

* [Managing user settings with Azure Multi-Factor Authentication in the cloud](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-manage-users-and-devices)<br>
* [Manage and support user accounts](https://docs.microsoft.com/azure/active-directory/authentication/multi-factor-authentication-faq)