<properties
    pageTitle="Problem deleting an Azure AD tenant"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565595"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# Problem deleting an Azure AD tenant 

## **Recommended steps**
1.	In order to delete an Azure AD, you need to be a Global Administrator on the directory. Ensure you are NOT signed in with an account that has the default directory such as contoso.onmicrosoft.com in the signed--in account, such as admin@contoso.onmicrosoft.com. 
2.	If there are any active applications in the directory, they must be removed before deletion can occur. Navigate to App registrations and remove the existing applications. 
3.	Ensure there are no active subscriptions for any Microsoft Online Services, such as Microsoft Azure, Office 365 or Azure AD Premium associated on the directory you are trying to delete. You must transfer your subscriptions or expedite cancellation of active subscriptions via Azure Support and Billing. Learn more on How to Cancel Office 365 and Azure subscriptions. 
4.	Check that there are no other active users in the directory besides yourself as the Global Administrator when attempting to delete the Azure AD. Remove any other active users, and any dependencies on a custom domain name in the tenant will also need to be removed, such as users created with admin@contoso.com. 

## **Recommended documents**

* [How Azure subscriptions are associated with Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory)

* [Deleting Users from Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)

* [Removing applications in the directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#removing-an-application)

* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)

* [Additional information on deleting an Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-administer#how-can-i-delete-an-azure-ad-directory) 

