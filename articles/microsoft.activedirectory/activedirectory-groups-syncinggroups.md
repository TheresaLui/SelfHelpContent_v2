<properties 
    pageTitle="Synchronizing a group between on-premises and the cloud"
    description="Synchronizing a group between on-premises and the cloud"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="krbain"
    selfHelpType="generic"
    supportTopicIds="32586796"
    productPesIds="14785"
    cloudEnvironments="public"
/>

# Synchronizing a group between on-premises and the cloud

## **Recommended steps**

1. If a global admin or group owner is not able to modify group properties, add members or assign owners in the Azure portal, please ensure the source of the authority for the group is Azure Active Directory to modify the group.<br>
2. Before attempting to delete a synced group in Azure Active Directory, ensure you have [deleted all assigned licenses](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-group-advanced#deleting-a-group-with-an-assigned-license) to avoid errors.<br>


## **Recommended documents**

* [Syncing an on-premises group to Azure using Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect)
* [Deleting a group with an assigned license](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-group-advanced#deleting-a-group-with-an-assigned-license)
