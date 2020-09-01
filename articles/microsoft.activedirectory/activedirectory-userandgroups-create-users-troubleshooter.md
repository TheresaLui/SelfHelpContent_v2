<properties 
    pageTitle="I can't create a new user in my Azure AD"
    description="I can't create a new user in my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="2500"
    selfHelpType="resource"
    resourceTags="userandgroups_overview,userandgroups_user"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="d76aa3c6-0e07-4cbe-b420-7007cd993250"
	ownershipId="AzureIdentity_User"
/>
# I can’t create a new user in my Azure AD

## **Recommended steps**
1. Ensure that you are authorized to create a new standard user. Only a global administrator or user administrator of Azure AD can create a new standard user. If you are not in one of these roles, you must have an administrator create the new user for you, or add you to one of these roles.  [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2. Ensure that the user name is in a domain that is not federated to Azure AD from your on-premises AD. Users cannot be added in the cloud with domain names that are federated with your Azure AD.
3. Ensure that no other user or contact already has the user name that you want to assign to the new user. User names must be unique across Azure AD.

## **Recommended documents**

* [Use the Azure portal to create a new user in your Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal) 
* [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) 
* [Use Azure AD PowerShell to create a new user](https://docs.microsoft.com/powershell/azuread/v2/new-azureaduser)

