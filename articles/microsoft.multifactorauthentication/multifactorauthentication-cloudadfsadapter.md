<properties
  pageTitle="Cloud-based MFA/Installing or configuring cloud-based MFA AD FS adapter"
  description="Installing or configuring cloud-based MFA AD FS adapter"
  service="microsoft.multifactorauthentication"
  resource=""
  authors="kgremban"
  selfHelpType="generic"
  supportTopicIds="32570991"
  productPesIds="14947"
  cloudEnvironments="public"
/>

# Installing or configuring cloud-based MFA AD FS adapter

## **Recommended steps**

If you are configuring AD FS Adapter for cloud-based MFA on Server 2016, the AD FS adapter may be used for either primary authentication or secondary authentication. When used for primary authentication, users must use verifications from the mobile app as their verification method. When used for secondary authentication, all registered method are available to users (phone call, text message, mobile app notifications, and mobile app verifications codes).

When considering the AD FS adapter for secondary authentication, there are other alternatives:

1. For web-based apps, it likely will make more sense to have MFA performed by AAD.

2. For on-premises apps, AAD Application Proxy could be used instead with MFA performed by AAD. 

## **Recommended documents**

- [Configure AD FS 2016 and Azure MFA](https://technet.microsoft.com/windows-server-docs/identity/ad-fs/operations/configure-ad-fs-2016-and-azure-mfa) 
- [Getting started with Active Directory Application Proxy](https://docs.microsoft.com/azure/active-directory/active-directory-application-proxy-get-started) 
- [Securing cloud resources with Azure Multi-Factor Authentication and AD FS](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud)