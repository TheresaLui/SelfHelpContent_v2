<properties
    pageTitle="Problems with other device issues in Azure AD"
    description="Device registration support self-help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="spunukol"
    ms.author="spunukol"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32596857"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="b0aedf00-9a6b-4170-9f34-d46fa62e0dd3"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problems with other issues with devices in Azure AD

## **Recommended Steps**

1. If you are setting up device registrations for the first time, please ensure that you have reviewed [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction) that will guide you on how to get devices under the control of Azure AD
2. If you are registering devices into Azure AD directly and enrolling them into Intune, you will need to ensure that you have [configured Intune](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment) and have the [licensing](https://docs.microsoft.com/mem/intune/fundamentals/licenses-assign) in place first
3. Ensure you are authorized to perform operations in Azure AD and on-premises AD. Only a global administrator in Azure AD can manage settings for device registrations. In addition, if you are setting up automatic registrations in your on-premises Active Directory, you will need to be an administrator of Active Directory and AD FS (if applicable).

## **Recommended Documents**

### Set up and manage device registrations

* [Set up Azure AD joined devices](https://docs.microsoft.com/azure/active-directory/devices/azuread-joined-devices-frx)<br>
* [Set up hybrid Azure AD joined (on-premises domain-joined) devices](https://docs.microsoft.com/azure/active-directory/device-management-hybrid-azuread-joined-devices-setup)<br>
* [Manage devices using the Azure portal](https://docs.microsoft.com/azure/active-directory/device-management-azure-portal)

### Troubleshooting common issues for registration and managing devices

* [Troubleshooting hybrid Azure AD Windows 10 and Windows Server 2016 registrations](https://docs.microsoft.com/azure/active-directory/device-management-troubleshoot-hybrid-join-windows-current)<br>
* [Troubleshooting hybrid Azure AD Windows 7 and non-Windows 10/Windows Server 2016 (down-level) registrations](https://docs.microsoft.com/azure/active-directory/device-management-troubleshoot-hybrid-join-windows-legacy)<br>
* [Frequently asked questions for device registration](https://docs.microsoft.com/azure/active-directory/device-management-faq)
