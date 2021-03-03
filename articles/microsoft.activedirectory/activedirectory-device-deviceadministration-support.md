<properties
    pageTitle="Problems with device administration in Azure AD"
    description="Device registration support self-help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="spunukol"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32596847"
    resourceTags=""
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="563a3c25-0167-4c2c-8d23-e522d5ee9c70"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problems with device administration in Azure AD

## **Recommended steps**

1. If you are setting up device registrations for the first time, please ensure that you have reviewed [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/overview) that will guide you on how to get devices under the control of Azure AD.
2. If you are registering devices into Azure AD directly and enrolling them into Intune, you will need to ensure that you have [configured Intune](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment) and have the [licensing](https://docs.microsoft.com/mem/intune/fundamentals/licenses-assign) in place first.
3. Ensure you are authorized to perform operations in Azure AD and on-premises AD. Only a global administrator in Azure AD can manage settings for device registrations.  In addition, if you are setting up automatic registrations in your on-premises Active Directory, you will need to be an administrator of Active Directory and AD FS (if applicable).

## **Recommended documents**

### Setup and manage device registrations ###

* [Manage devices using the Azure portal](https://docs.microsoft.com/azure/active-directory/devices/device-management-azure-portal)

### Troubleshooting common issues for registration and managing Azure AD devices ###

* [Troubleshooting hybrid Azure AD Windows 10 and Windows Server 2016 registrations](https://docs.microsoft.com/azure/active-directory/devices/troubleshoot-hybrid-join-windows-current)

* [Troubleshooting hybrid Azure AD Windows 7 and non-Windows 10/Windows Server 2016 (down-level) registrations](https://docs.microsoft.com/azure/active-directory/devices/troubleshoot-hybrid-join-windows-legacy)

* [Frequently asked questions for device registration](https://docs.microsoft.com/azure/active-directory/devices/faq)