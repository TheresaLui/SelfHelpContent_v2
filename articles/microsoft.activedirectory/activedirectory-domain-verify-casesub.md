<properties
    pageTitle="Resolve issues with Azure Active Directory domain name verification"
    description="Resolve issues with Azure Active Directory domain name verification"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    ms.author="elkuzmen"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045779"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="dd4bebf8-60fe-4958-9148-2ce1689957c9"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Resolve issues with Azure Active Directory domain name verification

## **Recommended Steps**

1. Ensure that you have correctly [configured your TXT/MX record](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#add-the-dns-entry-at-the-domain-name-registrar-for-the-domain) with your domain name registrar. It may take up to 72 hours to propagate as Verified.
2. If you have previously configured your domain name with another Azure AD tenant or in Office 365, you must [troubleshoot the domain from the existing tenant](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#troubleshooting). You cannot have the same custom domain name verified on two different tenants. It will fail to verify by design.
3. If you have users who have activated PowerBI via self-service sign-up and have created an unmanaged tenant for your organization, the IT admin can manage this tenant via takeover or can proceed to [add the domain with force takeover option](https://powerbi.microsoft.com/documentation/powerbi-admin-administering-power-bi-in-your-organization/#what-is-the-process-to-manage-a-tenant-created-by-Microsoft-for-my-users) in PowerShell.

## **Recommended Documents**

* [Add a custom domain name in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain)<br>
* [Federated and managed domain names](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#federated-and-managed-domain-names)
