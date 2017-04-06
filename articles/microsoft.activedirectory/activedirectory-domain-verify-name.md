<properties
	pageTitle="I can't verify my domain name even though I added it to Azure AD"
	description="Azure Active Directory domains troublehooter"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="Jeffsta-MSFT"
	displayOrder="4291"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="directory_domain"
	productPesIds=""
	cloudEnvironments="public"
/>

# I can't verify my domain name even though I added it to Azure AD

## **Recommended steps**

1. Ensure that you have correctly configured your TXT/MX record with your domain name registrar. [Learn more.](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#add-the-dns-entry-at-the-domain-name-registrar-for-the-domain)

2. If you have previously configured your domain name with another Azure AD tenant or Office 365 tenant, you must troubleshoot the domain from the portal in which you created the existing tenant. [Learn more](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#troubleshooting)

3. If you have users who have activated PowerBI via self-service sign-up and have created an unmanaged tenant for your organization, the IT admin can manage this tenant via takeover. [Learn more](https://powerbi.microsoft.com/documentation/powerbi-admin-administering-power-bi-in-your-organization/#what-is-the-process-to-manage-a-tenant-created-by-Microsoft-for-my-users).

## **Recommended documents**

[Add a custom domain name in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain)

[Federated and managed domain names](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#federated-and-managed-domain-names)

