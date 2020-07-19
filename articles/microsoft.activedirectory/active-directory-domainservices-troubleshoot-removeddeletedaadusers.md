<properties
	pageTitle="Problem removing deleted Azure AD users from your managed domain"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="arluca"
	selfHelpType="resource"
	displayOrder="300"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="7c5abfda-96f0-4837-ba03-d7a3363a3ed5"
	ownershipId="AzureIdentity_DomainName"
/>

# Problem removing deleted Azure AD users from your managed domain
Azure AD protects you from accidental deletion of user objects. When you delete a user account from your Azure AD tenant, the corresponding user object is moved to the Recycle Bin. When this delete operation is synchronized to your managed domain, it causes the corresponding user account to be marked disabled, even if you re-create a user account with the same UPN in your Azure AD directory.

## **Recommended steps**
To delete the user from your managed domain, you must first delete the user permanently from your Azure AD tenant:
*  Use the Remove-MsolUser PowerShell cmdlet with the '-RemoveFromRecycleBin' option, as described in this [MSDN article](https://msdn.microsoft.com/library/azure/dn194132.aspx).

## **Recommended documents**
* [Azure AD Domain Services FAQs](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)
