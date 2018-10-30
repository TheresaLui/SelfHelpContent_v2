<properties
    pageTitle="Recover RBAC when subscriptions are moved across tenants"
    description="Azure Active Directory troubleshooting"
    infoBubbleText=""
    service=microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    displayOrder=""
    articleId=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32615428"
    resourceTags=""
    productPesIds="16578"​
    cloudEnvironments="public"
/>

# Recover RBAC when subscriptions are moved across tenants

## **Recommended steps**

If you transfer a subscription to a new Azure AD tenant, all role assignments in RBAC are permanently deleted from the source tenant and are not migrated to the target tenant. You must re-create the role assignments in the target tenant. [Learn more](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
