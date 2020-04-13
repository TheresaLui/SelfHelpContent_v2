<properties  
    pageTitle="Cloud-based MFA/Configuring Azure MFA Settings"
    description="Troubleshooting issues with Azure MFA Settings"
    service="microsoft.multifactorauthentication"
    resource=""
    authors="kgremban"
    selfHelpType="generic"
    supportTopicIds="32570990"
    productPesIds="14947,16579"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    	articleId="9e0b4d86-a819-4f6a-8d67-3c9b72d1ed8f"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Configuring Azure MFA Settings

## **Recommended steps**

1. **Licensing enforcement** – it is your responsibility to ensure that you have the appropriate licenses for Azure MFA. The Azure MFA portal does not verify that you have sufficient licenses for all users and admins that you choose to protect with Azure MFA.

2. **Registration** – to use Azure MFA, users must first register a verification method. If you enable per-user MFA by setting the user’s MFA state to ‘enabled’, the user will be prompted to register security information on their next sign-on. If you use Conditional Access to require MFA, you should keep the user’s MFA state ‘Disabled’, and instead point the users to the MFA registration portal (https://aka.ms/mfasetup -> Additional Security Verification), or use an MFA registration policy to register users for MFA.

3. **Automating MFA registration** – while you can use PowerShell to set the user’s MFA status, there is currently no way to programmatically pre-register the user’s phone number for MFA.

## **Recommended documents** 

- [Getting started with Azure Multi-Factor Authentication in the cloud](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-cloud)
- [Multi-Factor Authentication registration policy](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection#multi-factor-authentication-registration-policy)
- [How to get Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans#how-to-get-azure-multi-factor-authentication-1) 