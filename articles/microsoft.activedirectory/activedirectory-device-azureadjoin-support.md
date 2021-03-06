<properties
  pagetitle="Problems with Azure AD Join"
  description="Device registration support self-help"
  service="microsoft.aad"
  resource="microsoft_aad_iam"
  ms.author="juquint"
  selfhelptype="Generic"
  supporttopicids="32596840"
  resourcetags=""
  productpesids="14785,16578"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="8e507143-2943-404b-ada1-0ce1df865cc2"
  ownershipid="AzureIdentity_DirectoryObjectManagement" />
# Problems with Azure AD Join

This article can help you troubleshoot and resolve most common issues around registration and managing Azure AD joined devices.

 **Highly Recommended**

1. Troubleshoot the most common device registration issues by leveraging the comprehensive [Device Registration Troubleshooter Tool](https://docs.microsoft.com/samples/azure-samples/dsregtool/dsregtool/).
2. Ensure that a device can access Device Registration endpoints under the system account by using the [Test Device Registration Connectivity script](https://docs.microsoft.com/samples/azure-samples/testdeviceregconnectivity/testdeviceregconnectivity/).
3. Seek and manage stale devices in your environment by using the [Azure AD Device Cleanup Script](https://github.com/mzmaili/AzureADDeviceCleanup).

## **Recommended steps**

1. If you're setting up device registrations for the first time, ensure that you have reviewed [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/overview) that will guide you on how to get devices under the control of Azure AD
2. If you're registering devices into Azure AD directly and enrolling them into Intune, you need to ensure that you have [configured Intune](https://docs.microsoft.com/mem/intune/enrollment/device-enrollment) and have the [licensing](https://docs.microsoft.com/mem/intune/fundamentals/licenses-assign) in place first
3. Ensure that you're authorized to perform operations in Azure AD. Only a global administrator in Azure AD can manage settings for device registrations.

## **Recommended documents**

### Plan, setup, and manage Azure AD joined devices

* [Plan Azure AD Join](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan)

* [Set up Azure AD joined devices](https://docs.microsoft.com/azure/active-directory/devices/azuread-joined-devices-frx)

* [Set up Azure AD joined devices during Windows 10 first-run experience](https://docs.microsoft.com/azure/active-directory/devices/azuread-joined-devices-frx)

* [Manage devices using the Azure portal](https://docs.microsoft.com/azure/active-directory/devices/device-management-azure-portal)

* [Frequently asked questions for device registration](https://docs.microsoft.com/azure/active-directory/devices/faq)
