<properties
    pageTitle="Problems enrolling devices with Azure AD"
    description="Problems enrolling devices with Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="a5c9574d-e895-43c8-816c-b85e71ec1b3c"
	ownershipId="AzureIdentity_User"
/>

# Problems enrolling devices with Azure AD

**I don't know how to enroll Windows 7 PCs with Azure AD**

Windows 7 PCs that are domain joined to an on-premises Active Directory can also be enrolled with Azure AD. Conditional access policy can then be applied to require a domain joined machine when accessing specified cloud applications.
<br><br>
For more details, see:
<br>
[How to set up Conditional Access for Windows 7 devices](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup)


**I don't know how to increase the number of devices users can register**

In the Azure AD portal, you can set the maximum number of devices that a user can have in Azure AD. If a user reaches this quota, they will not be able to add additional devices until one or more of their existing devices are removed.
<br><br>
For more details, see:
<br>
[How to set the number of devices a user can register](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-setup)


**I encountered a problem where conditional access always blocks my device**

When a policy that requires a compliant of domain join device fails it may be because the device is not registered correctly with Azure AD. Devices must be registered with Azure AD so information about the device is available when the user authenticates and policy is applied. You can verify device information using PowerShell to read the device properties in Azure AD. 
<br><br>
For more details, see:
<br>
[How to verify device information in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup)