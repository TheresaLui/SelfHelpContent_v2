<properties
    pageTitle="Problems with on-premises AD device registrations to Azure AD"
    description="Device registration support self-help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="spunukol"
    ms.author="marwa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32596850"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="ca67522e-d5a6-4e4b-af04-c9e7d417e1a9"
    ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problems with on-premises AD device registrations to Azure AD (Hybrid Azure AD join)

**Highly Recommended** Ensure that a device can access Device Registration endpoints under the system account by using the [Test Device Registration Connectivity script](https://gallery.technet.microsoft.com/Test-Device-Registration-3dc944c0)

## **Recommended Steps**

1. If you are setting up device registrations for the first time, be sure to review [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/overview) to learn how to get devices under the control of Azure AD.
2. If you are registering devices into Azure AD directly and enrolling them into Intune, be sure that you've [configured Intune](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment) and have the [licensing](https://docs.microsoft.com/mem/intune/fundamentals/licenses-assign) in place first.
3. Ensure that you are authorized to perform operations in Azure AD and on-premises AD. Only a global administrator in Azure AD can manage settings for device registrations. In addition, if you are setting up automatic registrations in your on-premises Active Directory, you will need to be an administrator of Active Directory and AD FS (if applicable).


## **Recommended Documents**

### Set up and manage device registrations to Azure AD for on-premises AD ###
* [Set up hybrid Azure AD joined (on-premises domain-joined) devices](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan)
* [Manage devices using the Azure portal](https://docs.microsoft.com/azure/active-directory/devices/device-management-azure-portal)

### Troubleshooting common issues for registration and managing Hybrid Azure AD joined devices ###
* [Troubleshooting hybrid Azure AD Windows 10 and Windows Server 2016 registrations](https://docs.microsoft.com/azure/active-directory/devices/troubleshoot-hybrid-join-windows-current)
* [Troubleshooting hybrid Azure AD Windows 7 and non-Windows 10/Windows Server 2016 (down-level) registrations](https://docs.microsoft.com/azure/active-directory/devices/troubleshoot-hybrid-join-windows-legacy)
* [FAQ for device registration](https://docs.microsoft.com/azure/active-directory/devices/faq)
