<properties  
    pageTitle="Cloud-based MFA/Installing or configuring Azure MFA NPS extension" 
    description="Installing or configuring extensions for MFA service (cloud)" 
    service="microsoft.multifactorauthentication" 
    resource="" 
    authors="kgremban" 
    selfHelpType="generic" 
    supportTopicIds="32565586" 
    productPesIds="14947" 
    cloudEnvironments="public"
    />
 
# Installing or configuring extensions for MFA service (cloud)  
## **Recommended steps** 
Follow these steps to troubleshoot common scenarios with the NPS Extension for Azure MFA: 

**ADAL token error**
<!---Loc Comment: The matada seems to be incorrect--->
1. Restart your NPS Server. 
2. Verify that the client cert is installed as expected. 
3. Verify that the certificate is associated with your tenant on AzureAD. 
4. Verify that https://login.windows.net/ is accessible from the server running the extension. 

**HTTP logs show user not found error**

1. Verify that AD Connect is running. 
2. Verify that the user is present in both Windows Active Directory and Azure Active Directory. The presence of a user is determined by the UPN or alternate login-Id. They should be in sync between On-Prem AD and Azure AD. 

**NoDefaultAuthenticationMethodIsConfigured and ProofDataNotFound**

1. Verify that the user has registered for Azure MFA and set up at least one verification method. 

**HTTP connect errors in logs and all auths are failing**

1. Verify that https://adnotifications.windowsazure.com is reachable from the server running the NPS extension. 

## **Recommended documents** 
  
- [Integrate your existing NPS infrastructure with Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-nps-extension) 
- [Resolve error messages from the NPS extension for Azure Multi-Factor Authentication](https://review.docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-nps-errors?branch=pr-en-us-10717)
