<properties
    pageTitle="Problems with device registrations and managing devices in Azure AD"
    description="Device registration"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="spunukol"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32392474"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>

# Problems with device registrations and managing devices in Azure AD

## **Recommended steps**

1. Ensure you are authorized to perform operations in Azure AD and on-premises AD. Only a global administrator in Azure AD can manage settings for device registrations. In addition, if you are setting up automatic registrations in your on-premises Active Directory, you will need to be an administrator of Active Directory and AD FS (if applicable).
2. If you are registering devices into Azure AD directly and enrolling them into Intune, you will need to ensure that you have [configured Intune](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune) and have the [licensing](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune-step-3) in place first.
3. If you are setting up automatic device registration for on-premises AD devices for the first time, please ensure that [all pre-requisites listed in the document](https://docs.microsoft.com/azure/active-directory/active-directory-device-registration-overview) are in place.  


## **Recommended documents**
### Set up Azure AD ###

* [Set up to join Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-overview) 

### Set up device registration ###

* [Set up automatic registration for on-premises Active Directory devices](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup) 

### Troubleshooting common issues for registration and managing devices ###

* [Troubleshooting Windows 10 and Windows Server 2016 registration](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows)

* [Troubleshooting Windows 7 and non-Windows 10/Windows Server 2016 registrations](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows-legacy)

* [Frequently asked questions for device registration](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-faq) 

