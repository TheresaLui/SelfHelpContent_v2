<properties
	pageTitle="MFA Server (On-Premises)/Other questions regarding MFA server (on-premises)"
	description="MFA Server (On-Premises)/Other questions regarding MFA server (on-premises)"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="kgremban"
	displayOrder="260"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="mfa_overview"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8be9edc6-1654-4758-a453-c996864024f0"
	ownershipId="AzureIdentity_User"
/>

# Other questions about MFA Server

## **Recommended steps**

If you're having trouble creating an MFA provider, verify that you need one. In most cases, you don't. An Azure Multi-Factor Auth provider is for users who don't have licenses through Azure MFA, Azure AD Premium, or EMS but still want to take advantage of the features provided by the full version of Azure MFA. If you have these licenses that include the full version of Azure MFA by default, then you don't need an MFA provider. 

If you're having trouble syncing users from Active Directory to MFA Server, use these steps:

1. Check MultiFactorAuthSvc.log and MultiFactorAuthAdSyncScv.log for errors. 
2. Check the Directory Integration settings on the MFA Server that is running the AD sync service. If **Use specific LDAP directory** is selected, make sure that the bind username/DN and bind password are correct. Verify them with the **Test** button. 
3. Make sure that **Use attribute scope queries** is unchecked. This option is not needed, and checking it can cause issues. 
4. Go to the **Synchronization** tab and make sure that **Always perform a full synchronization** is selected. Delta sync is not recommended.

## **Recommended documents**

- [Getting started with the Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server)  
- [Getting started with an Azure Multi-Factor Auth Provider](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-auth-provider)  
- [LDAP Authentication and Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-LDAP)  
- [Upgrade to the latest Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-server-upgrade)  
