<properties
    pageTitle="Licensing"
    description="Licensing"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="SumitParikh"
    displayOrder="1770"
    supportTopicIds="32570956"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="875c437a-f5d4-4735-a7d3-11d84fb6e4de"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Licensing

**Things to check first**

1. To manage licenses, you must use an account with one of the required [administrator roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles): Global Administrator or User Account Administrator. You can check the user’s role in the **Roles and administrators** tab on the Overview blade.
2. If you are using the Azure portal and license assignment is failing, make sure to click the notification in the upper-right corner. This opens a blade with details about what went wrong. In most cases that is enough to understand and resolve the problem.
3. Learn more about how to Assign or remove Azure Active Directory licenses [here](https://docs.microsoft.com/azure/active-directory/fundamentals/license-users-groups?).
4. Learn more about what Azure Active Directory features are available for different Azure Active Directory editions [here](https://azure.microsoft.com/pricing/details/active-directory/)

## **Recommended steps**

1. Is your problem related to per-user subscriptions (e.g. Office 365, Enterprise Mobility + Security, Dynamics 365, etc.) or an Azure resource subscription (e.g. virtual machines, storage accounts)? For Azure resource subscription problems, make sure to open the support ticket under "Subscription problems".
2. If you are using dynamic groups to manage your user’s membership, verify that the user is part of the group, which is necessary for license assignment. If not, [check processing status for the membership rule](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-create-rule#check-processing-status-for-a-membership-rule) of the dynamic group. If there is processing problem, make sure to open the support ticket under Group Management.
3. Before a license can be assigned to a user, the Usage Location property must be set for the user. Verify the user has that property set by viewing the Profile tab on the user blade.