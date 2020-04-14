<properties
    pageTitle="Problem deleting a domain name"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045808"
    resourceTags=""
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="e4bba8f2-9a44-42aa-af12-572d84062eb6"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem deleting a domain name

## **Recommended steps**
1.	To delete a custom domain name, ensure you have removed all users, groups and applications dependent on the custom domain name. If there are any existing resources using the domain name, the deletion will not succeed. 
2.	Ensure the account you are signed in with is NOT admin@contoso.com when you are trying to delete the tenant “contoso.com”, because that deletion won't work. You must use a Global Admin account that does not have a dependency on the custom domain name you are trying to delete, and instead use the initial default domain name like admin@contoso.onmicrosoft.com and sign in to delete the domain name. Or you can use another Global Admin account with different verified domain name like admin@contosocorp.com to delete “contoso.com” in the directory. 
3.	If you are attempting to delete the initial default Azure AD domain name such as “contoso.onmicrosoft.com”, you can't because this third-level domain is established on directory creation. This initial domain name is intended primarily for bootstrapping until your custom domain name is verified.
4.	In the case you wish to use your existing .onmicrosoft.com domain like “contoso.onmicrosoft.com” on another Azure AD tenant or Office 365, you must delete the existing directory and create a new instance with the same initial default name “contoso.onmicrosoft.com”. Data will not transfer to the new tenant, and domain name deletion is irreversible. 


## **Recommended documents**
* [Manage your initial default .onmicrosoft.com domain name](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#initial-and-custom-domain-names)<br>
* [Deleting users from Azure AD]( https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)<br>
* [Removing an application in your directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications)<br>
* [Resource dependencies on domains](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence)<br>
* [Use PowerShell or Graph API to manage domain names](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#use-powershell-or-graph-api-to-manage-domain-names)