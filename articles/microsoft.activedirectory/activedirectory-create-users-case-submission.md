 <properties 
    pageTitle="Problem creating, updating, or deleting a user in Azure AD"
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

# I can’t create a new user in my Azure AD

## **Recommended steps**

1. Ensure that you are authorized to perform this operation. Only a global administrator or user administrator in Azure AD can create, update or delete an existing user. If you are not in one of these roles, you must have an administrator create the new user for you, or add you to one of these roles. [Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2. If you are creating a new user, ensure that the user name is unique, and is in a domain that is not federated to Azure AD from your on-premises AD. User names are unique across Azure AD. Users cannot be added in the cloud with domain names that are federated with your Azure AD.
3. If you are updating a user, ensure that you are not updating a property that is synced from your on-premises AD. If the user is synced (that is, if Source = ‘Windows Server AD’), then the only properties that can be managed in Azure AD are in the ‘Settings’ and ‘Authentication contact info’ sections. To change any other property, change it in your on-premises directory. You’ll see the updated property in the cloud after the next time sync runs.
4. If you are deleting a user, ensure that the user is not synced from your on-premises AD. If the user is synced (that is, if Source = ‘Windows Server AD’), then delete the user in your on-premises directory. Then after sync has run, you will see that the user has been deleted from Azure AD.

## **Recommended documents**

[Azure AD administrative roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) 
[Use the Azure portal to create a new user in your Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal) 
[Use the Azure portal to delete a user in your Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal) 
[Use Azure AD PowerShell to manage users](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#users)
