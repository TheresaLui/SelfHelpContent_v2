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
    cloudEnvironments="public"
/>

# Problems with device registrations and managing devices in Azure AD

## **Recommended steps**

1. Ensure that you are authorized to perform operations in Azure AD and in your on-premises AD. Only global administrators in Azure AD can manage settings for device registrations. In addition, if you are setting up automatic registrations in your on-premises Active Directory, you need to be an administrator of Active Directory and AD FS (if applicable).
	
2. If you are registering devices into Azure AD directly and enrolling them into Intune, you need to ensure that you have configured Intune and have the licensing in place, first.
	
3. If you are setting up automatic device registration for on-premises AD devices for the first time, please ensure that all prerequisites listed in the document are in place.
   
4.	Before you submit the ticket, we recommend that you review the documents listed here. They help with the setup of Azure AD and device registrations and troubleshooting.


## **Recommended documents**
### Setup Azure AD ###

[Setup to join Azure AD] (https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-overview) 

### Setup device registration ###

[Setup automatic registration for on premises Active Directory devices] (https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup) 

### Troubleshooting common issues for registration and managing devices ###

[Troubleshooting Windows 10 and Windows Server 2016 registration] (https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows)  
[Troubleshooting Windows 7 and non-Windows 10/Windows Server 2016 registrations] (https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows-legacy)  
Frequently asked questions for device registration] (https://docs.microsoft.com/en-us/azure/active-directory/active-directory-conditional-access-automatic-device-registration-faq) 

