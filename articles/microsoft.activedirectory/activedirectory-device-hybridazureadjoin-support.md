<properties
  pagetitle="Problems with on-premises AD device registrations to Azure AD (Hybrid Azure AD join)"
  description="Device registration support self-help"
  service="microsoft.aad"
  resource="microsoft_aad_iam"
  ms.author="juquint"
  selfhelptype="Generic"
  supporttopicids="32596850"
  resourcetags=""
  productpesids="16578"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="ca67522e-d5a6-4e4b-af04-c9e7d417e1a9"
  ownershipid="AzureIdentity_DirectoryObjectManagement" />
# Problems with on-premises AD device registrations to Azure AD (Hybrid Azure AD join)

Resolve issues with on-premises AD device registrations to Azure AD using the following steps.

**Highly Recommended**

1. Troubleshoot the most common device registration issues by leveraging the comprehensive [Device Registration Troubleshooter Tool](https://docs.microsoft.com/samples/azure-samples/dsregtool/dsregtool/)
2. Ensure that a device can access Device Registration endpoints under the system account by using the [Test Device Registration Connectivity script](https://docs.microsoft.com/samples/azure-samples/testdeviceregconnectivity/testdeviceregconnectivity/) 

## **Recommended Steps**

1. If you're setting up device registrations for the first time, be sure to review [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/overview) to learn how to get devices under the control of Azure AD.
2. If you're registering devices into Azure AD directly and enrolling them into Intune, be sure that you've [configured Intune](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment) and have the [licensing](https://docs.microsoft.com/mem/intune/fundamentals/licenses-assign) in place first.
3. Ensure that you're authorized to perform operations in Azure AD and on-premises AD. Only a global administrator in Azure AD can manage settings for device registrations. In addition, if you're setting up automatic registrations in your on-premises Active Directory, you'll need to be an administrator of Active Directory and ADFS, if applicable.


## **Recommended Documents**

### Set up and manage device registrations to Azure AD for on-premises AD ###
* [Set up hybrid Azure AD joined (on-premises domain-joined) devices](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan)
* [Manage devices using the Azure portal](https://docs.microsoft.com/azure/active-directory/devices/device-management-azure-portal)

### Troubleshoot common issues when registering and managing Hybrid Azure AD joined devices ###
* [Troubleshooting hybrid Azure AD Windows 10 and Windows Server 2016 registrations](https://docs.microsoft.com/azure/active-directory/devices/troubleshoot-hybrid-join-windows-current)
* [Troubleshooting hybrid Azure AD Windows 7 and non-Windows 10/Windows Server 2016 (down-level) registrations](https://docs.microsoft.com/azure/active-directory/devices/troubleshoot-hybrid-join-windows-legacy)
* [FAQ for device registration](https://docs.microsoft.com/azure/active-directory/devices/faq)