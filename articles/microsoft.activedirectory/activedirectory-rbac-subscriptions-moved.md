<properties
    pageTitle="Recover RBAC when subscriptions are moved across tenants"
    description="Azure Active Directory troubleshooting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    ms.author="rolyon"
    displayOrder=""
    articleId="6a973647-50e6-4954-ace9-5b1844cf0657"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32690726"
    resourceTags=""
    productPesIds="16986"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_RBAC"
/>

# Azure Active Directory: Recover RBAC when subscriptions are moved across tenants

## **Recommended Steps**

* If you need steps for how to transfer a subscription to a different Azure AD tenant, see [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* If you transfer a subscription to a different Azure AD tenant, all role assignments are permanently deleted from the source Azure AD tenant and are not migrated to the target Azure AD tenant. You must re-create your role assignments in the target tenant.
* If you are a Azure AD Global Administrator and you don't have access to a subscription after it was moved between tenants, use the **Access management for Azure resources** toggle to temporarily [elevate your access](https://docs.microsoft.com/azure/role-based-access-control/elevate-access-global-admin) to get access to the subscription

## **Recommended Documents**

- [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
- [Elevate access to manage all Azure subscriptions and management groups](https://docs.microsoft.com/azure/role-based-access-control/elevate-access-global-admin)
