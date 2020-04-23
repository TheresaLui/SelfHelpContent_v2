<properties 
    pageTitle="Problem reading user profile data in Azure AD"
    description="Problem reading user profile data in Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32615470"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="667f077c-c52d-4b67-a755-cf00bb506369"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem reading user profile data in Azure AD

## **Recommended steps**

1. Use the Azure AD PowerShell v2 cmdlet "Get-AzureADUser" with the Format-List parameter to see the value of all properties for a user in Azure AD, including properties which are not displayed in the Azure AD administration portal experience. For example, `Get-AzureADUser -ObjectId alice@contoso.com | Format-List`.
2. Use the Azure AD PowerShell v2 cmdlet "Get-AzureADUser" with the parameter -ExpandProperty to see all the value of all extension properties for a user. For example, `Get-AzureADUser -ObjectId alice@contoso.com | Select -ExpandProperty ExtensionProperty`.

## **Recommended documents**

* [Azure AD cmdlets for managing users](https://docs.microsoft.com/powershell/module/azuread/get-azureaduser?view=azureadps-2.0)
* [Azure AD cmdlets for working with extension attributes](https://docs.microsoft.com/powershell/azure/active-directory/using-extension-attributes-sample?view=azureadps-2.0)
