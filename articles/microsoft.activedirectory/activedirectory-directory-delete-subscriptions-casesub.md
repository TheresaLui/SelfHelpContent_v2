<properties
    pageTitle="Problems removing subscriptions"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615413"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="496e4000-6529-4e27-afc9-999f477f68fa"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Directory deletion problem with removing subscriptions

## **Recommended steps**

Azure AD directory deletion is blocked if you have active subscriptions on any Microsoft Online Services, such as Microsoft Azure, Office 365 or Azure AD Premium associated on the directory you are trying to delete. You will need to transfer your subscriptions or expedite cancellation of active subscriptions via Azure Support and Billing.   [Cancel an Office 365 subscription](https://support.office.com/en-us/article/Contact-Office-365-for-business-support-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b?ui=en-US&rs=en-US&ad=US).

1. Ensure you do not have active subscriptions in the Azure AD that you are trying to delete. The subscriptions must be in a Deprovisoned state to allow tenant deletion. An Expired or Canceled subscription is not sufficient to enable directory deletion. Learn more about [I have an expired subscription but can't delete the tenant](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto#i-have-an-expired-subscription-but-i-cant-delete-the-tenant).
2. In case of attempting to transfer subscription ownership on Pay-As-You-Go, Visual Studio, Action Pack, or BizSpark subscriptions, you may do so via a self-service transfer in the Account Center. Learn more on [Transferring Azure subscriptions to another Azure AD](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)

## **Recommended documents**
* [How to delete an Azure AD tenant](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto)
* [Using PowerShell to delete apps](https://docs.microsoft.com/powershell/module/azuread/remove-azureadapplication?view=azureadps-2.0)
