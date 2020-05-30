<properties 
    pageTitle="MFA Service (Cloud)/Other questions regarding MFA Service (cloud)"
    description="MFA Service (Cloud)/Other questions regarding MFA Service (cloud)"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="kgremban"
    displayOrder="150"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="mfa_overview"
    productPesIds=""
    cloudEnvironments="public, fairfax, usnat, ussec"
 	articleId="89d02013-7a35-407d-8153-efaaf9502d79"
	ownershipId="AzureIdentity_User"
/>

# Other questions about Azure MFA in the cloud

## **Recommended steps**
If you're having trouble creating an MFA provider, verify that you need one. In most cases, you don't. An Azure Multi-Factor Auth provider is for users who don't have licenses through Azure MFA, Azure AD Premium, or EMS but still want to take advantage of the features provided by the full version of Azure MFA. If you have these licenses that include the full version of Azure MFA by default, then you don't need an MFA provider.  

If you're trying to access the MFA Management Portal via the MFA Service Settings page, use these steps: 

1. Sign into the Azure classic portal as an administrator and select **Active Directory**. 
2. Click on your directory and then click the **Configure** tab. 
3. Under the multi-factor authentication section, select **Manage service settings**. 
4. At the bottom of the MFA Service Settings page, click the **Go to the portal** link.

## **Recommended documents**
 
- [Frequently asked questions about Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-faq)  
- [Getting started with the Azure Multi-Factor Authentication in the cloud](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-cloud)  
- [Getting started with an Azure Multi-Factor Auth Provider](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-auth-provider)  
- [Configure Azure Multi-Factor Authentication settings](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)  
- [User States in Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-user-states)  
- [Azure Multi-Factor Authentication End User Guide](https://docs.microsoft.com/azure/multi-factor-authentication/end-user/multi-factor-authentication-end-user)  
