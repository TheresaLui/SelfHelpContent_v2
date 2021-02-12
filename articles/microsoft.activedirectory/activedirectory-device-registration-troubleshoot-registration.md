<properties
    pageTitle="Problems with device registrations and managing devices in Azure AD"
    description="Problems with device registrations and managing devices in Azure AD "
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="spunukol"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="AzureADDeviceRegistration_Registration"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="d6000833-7d8b-4213-9774-63d79131397a"
	ownershipId="AzureIdentity_User"
/>

# Problems with device registrations and managing devices in Azure AD

## **Recommended steps**

1. If you are setting up device registrations for the first time, please ensure that you have reviewed [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction) that will guide you on how to get devices under the control of Azure AD.
2. If you are registering devices into Azure AD directly and enrolling them into Intune, you will need to ensure that you have [configured Intune](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune) and have the [licensing](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune-step-3) in place first.
3. Ensure you are authorized to perform operations in Azure AD and on-premises AD. Only a global administrator in Azure AD can manage settings for device registrations. In addition, if you are setting up automatic registrations in your on-premises Active Directory, you will need to be an administrator of Active Directory and AD FS (if applicable).


## **Recommended documents**

### Setup and manage device registrations ###

* [Set up Azure AD registered Windows 10 devices](https://docs.microsoft.com/azure/active-directory/device-management-azuread-registered-devices-windows10-setup) 

* [Set up Azure AD joined devices](https://docs.microsoft.com/azure/active-directory/device-management-azuread-joined-devices-setup)

* [Set up hybrid Azure AD joined (on-premises domain-joined) devices](https://docs.microsoft.com/azure/active-directory/device-management-hybrid-azuread-joined-devices-setup)

* [Manage devices using the Azure portal](https://docs.microsoft.com/azure/active-directory/device-management-azure-portal)

### Troubleshooting common issues for registration and managing devices ###

* [Troubleshooting hybrid Azure AD Windows 10 and Windows Server 2016 registrations](https://docs.microsoft.com/azure/active-directory/device-management-troubleshoot-hybrid-join-windows-current)

* [Troubleshooting hybrid Azure AD Windows 7 and non-Windows 10/Windows Server 2016 (down-level) registrations](https://docs.microsoft.com/azure/active-directory/device-management-troubleshoot-hybrid-join-windows-legacy)

* [Frequently asked questions for device registration](https://docs.microsoft.com/azure/active-directory/device-management-faq)
