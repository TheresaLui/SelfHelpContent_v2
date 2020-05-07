<properties
  pageTitle="Cloud-based MFA/Installing or configuring cloud-based MFA AD FS adapter"
  description="Installing or configuring cloud-based MFA AD FS adapter"
  service="microsoft.aad"
  resource="Microsoft_AAD_IAM"
  authors="kgremban"
  displayOrder="130"
  selfHelpType="resource"
  supportTopicIds=""
  resourceTags="mfa_overview"
  productPesIds=""
  cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d5c27f34-a973-4aa6-a0d4-619262c0c058"
	ownershipId="AzureIdentity_User"
/>

# Questions about the AD FS adapter for Azure MFA in the cloud

## **Recommended steps**

If you are configuring AD FS Adapter for cloud-based MFA on Server 2016, the AD FS adapter may be used for either primary authentication or secondary authentication. When used for primary authentication, users must use verifications from the mobile app as their verification method. When used for secondary authentication, all registered method are available to users (phone call, text message, mobile app notifications, and mobile app verifications codes).

When considering the AD FS adapter for secondary authentication, there are other alternatives:

1. For web-based apps, it likely will make more sense to have MFA performed by AAD.

2. For on-premises apps, AAD Application Proxy could be used instead with MFA performed by AAD. 

## **Recommended documents**

- [Configure AD FS 2016 and Azure MFA](https://technet.microsoft.com/windows-server-docs/identity/ad-fs/operations/configure-ad-fs-2016-and-azure-mfa) 
- [Getting started with Active Directory Application Proxy](https://docs.microsoft.com/azure/active-directory/active-directory-application-proxy-get-started) 
- [Securing cloud resources with Azure Multi-Factor Authentication and AD FS](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud)
