<properties
    pageTitle="I can't verify my domain name even though I added it to Azure AD"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4291"
    selfHelpType="generic"
    supportTopicIds="32045779"
    resourceTags=""
    productPesIds="14785,16578"
    cloudEnvironments="public"
    />

# I can't verify my domain name even though I added it to Azure AD

## **Recommended steps**

1. Ensure that you have correctly configured your TXT/MX record with your domain name registrar.  It may take up to 72 hours to propagate as Verified. [Learn more](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#add-the-dns-entry-at-the-domain-name-registrar-for-the-domain)

2. If you have previously configured your domain name with another Azure AD tenant or in Office 365, you must troubleshoot the domain from the existing tenant. You cannot have the same custom domain name verified on two different tenants. It will fail to verify by design. [Learn more](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#troubleshooting)

3. If you have users who have activated PowerBI via self-service sign-up and have created an unmanaged tenant for your organization, the IT admin can manage this tenant via takeover or can proceed to add the domain with force takeover option in PowerShell. Learn more about [admin domain takeover](https://powerbi.microsoft.com/documentation/powerbi-admin-administering-power-bi-in-your-organization/#what-is-the-process-to-manage-a-tenant-created-by-Microsoft-for-my-users).

## **Recommended documents**

[Add a custom domain name in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain)

[Federated and managed domain names](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#federated-and-managed-domain-names)

