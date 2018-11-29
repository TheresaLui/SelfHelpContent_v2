<properties
    pageTitle="I still have other problems related to domain name management"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
    displayOrder="4297"
    selfHelpType="generic"
    supportTopicIds="32565597"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# Other problems related to domain name management

## **Recommended steps**

1. If you are getting an error that says “Domain already configured on another tenant”, please ensure that your custom domain name hasn’t already been configured on another Azure AD or Office 365. A User in your organization may have already signed up self-service with that domain name. You will need to remove the domain name from the existing tenant where the domain name is already verified and add it to the new Azure AD. You can manage this tenant with admin takeover, learn more here in [Take over an unmanaged directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover).
2. When you try to sign up for an new Azure offer for education or non-profit, and you get a “tenant not found” error, this might be due to the domain you are using for sign-up being verified in another tenant. In that case, you need to take over the tenant where the domain is already verified, with admin takeover or can proceed to add the domain with force takeover option in [PowerShell](https://docs.microsoft.com/powershell/msonline/v1/confirm-msoldomain).
3. If you are trying to configure a custom domain name for federated single sign-on, and you do not have ADFS set-up, you will need to configure federation settings in your directory with the Azure AD Connect tool to use your custom domain name.
4. If you are attempting to delete an Azure AD tenant, there can be no active subscriptions for any Microsoft Online Services, such as Microsoft Azure, Office 365 or Azure AD Premium associated on the directory you are trying to delete. You will need to transfer your subscriptions or expedite cancellation of active subscriptions via Azure Support and Billing. Learn more in [Cancel an Office 365 subscription](https://support.office.com/article/Contact-Office-365-for-business-support-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b).  

## **Recommended documents**

* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)<br>
* [How to perform a DNS domain name takeover]( https://docs.microsoft.com/azure/active-directory/active-directory-self-service-signup#how-to-perform-a-dns-domain-name-takeover)<br>
[Add subdomains of a custom domain name](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#add-subdomains-of-a-custom-domain)<br>
* [Resource dependencies in Office 365 and Azure AD tenants](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence)<br>
* [Verify the Azure AD domain configured for federation](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom#verify-the-azure-ad-domain-selected-for-federation)<br>
* [Use PowerShell or Graph API to manage domain names](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#use-powershell-or-graph-api-to-manage-domain-names)
