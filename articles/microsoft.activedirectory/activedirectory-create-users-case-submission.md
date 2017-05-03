 <properties 
    pageTitle="Creating a user or group"
    description="Problem creating, updating, or deleting a user in Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="2500"
    selfHelpType="generic"
    supportTopicIds="32045780"
    productPesIds="14785"
    cloudEnvironments="public"
/>

# Creating a user or group

## **Recommended steps**

1. Ensure that you are authorized to perform this operation. Only a global administrator or user administrator in Azure AD can create a user. If you are not in one of these roles, you must have an administrator create the new user for you, or add you to one of these roles. [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2. If you are creating a new user, ensure that the user name is unique, and is in a domain that is not federated to Azure AD from your on-premises AD. User names are unique across Azure AD. Users cannot be added in the cloud with domain names that are federated with your Azure AD.

## **Recommended documents**

* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)

* [Use the Azure portal to create a new user in your Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal) 
* [Use Azure AD PowerShell to manage groups](https://docs.microsoft.com/powershell/module/Azuread/?view=azureadps-2.0#groups)

* [Use Azure AD PowerShell to manage users](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#users)
