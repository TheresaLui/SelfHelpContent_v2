<properties
    pageTitle="Receiving error about domain configured on another tenant"
    description="Azure Active Directory directory troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4299"
    selfHelpType="generic"
    supportTopicIds="32570974"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# Receiving error about domain configured on another tenant  

## **Recommended steps**

1.	The same custom domain name cannot be verified in two different tenants. If you have already configured your custom domain name in Office 365 and are trying to add it to another Azure AD tenant, the verification will fail. You must first remove it from the existing tenant where the domain name is already verified and add it to the new Azure AD tenant.
2.	If someone in your organization has used self-service sign-up for PowerBI or RMS, they may have created an unmanaged tenant. You can manage this tenant with admin takeover or can proceed to add the domain with force takeover option in PowerShell.

## **Recommended documents**

* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* [How to perform a DNS domain name takeover](https://docs.microsoft.com/azure/active-directory/active-directory-self-service-signup#how-to-perform-a-dns-domain-name-takeover)
* [Resource dependencies in Office 365 and Azure AD tenants](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence) 
