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
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="e3cae983-06b3-42da-a82c-622015a69e4b"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problems with device registrations and managing devices in Azure AD

## **Recommended steps**

1. If you are setting up device registrations for the first time, please ensure that you have reviewed [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction) that will guide you on how to get devices under the control of Azure AD.
2. If you are registering devices into Azure AD directly and enrolling them into Intune, you will need to ensure that you have [configured Intune](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune) and have the [licensing](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune-step-3) in place first.
3. Ensure you are authorized to perform operations in Azure AD and on-premises AD. Only a global administrator in Azure AD can manage settings for device registrations. In addition, if you are setting up automatic registrations in your on-premises Active Directory, you will need to be an administrator of Active Directory and AD FS (if applicable).


## **Recommended documents**

### Setup and manage device registrations ###

* [Set up Azure AD registered Windows 10 devices](https://docs.microsoft.com/azure/active-directory/devices/azuread-joined-devices-frx)

* [Set up Azure AD joined devices](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-device-options)

* [Set up hybrid Azure AD joined (on-premises domain-joined) devices](https://docs.microsoft.com/azure/active-directory/device-management-hybrid-azuread-joined-devices-setup)

* [Manage devices using the Azure portal](https://docs.microsoft.com/azure/active-directory/device-management-azure-portal)

### Troubleshooting common issues for registration and managing devices ###

* [Troubleshooting hybrid Azure AD Windows 10 and Windows Server 2016 registrations](https://docs.microsoft.com/azure/active-directory/device-management-troubleshoot-hybrid-join-windows-current)

* [Troubleshooting hybrid Azure AD Windows 7 and non-Windows 10/Windows Server 2016 (down-level) registrations](https://docs.microsoft.com/azure/active-directory/device-management-troubleshoot-hybrid-join-windows-legacy)

* [Frequently asked questions for device registration](https://docs.microsoft.com/azure/active-directory/device-management-faq)

