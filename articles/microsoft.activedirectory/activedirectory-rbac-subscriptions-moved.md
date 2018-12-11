<properties
    pageTitle="Recover RBAC when subscriptions are moved across tenants"
    description="Azure Active Directory troubleshooting"
    infoBubbleText=""
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    authorAlias="rolyon"
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

1. If you need steps for how to transfer a subscription to a different tenant, see [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer).
1. If you transfer a subscription to a different tenant and you don't see your role assignments, you must re-create the role assignments in the target tenant. All role assignments are permanently deleted from the source tenant and are not migrated to the target tenant.
1. If you are a Global Administration and you don't have access to a subscription, use the Access management for Azure resources switch to temporarily [elevate your access](https://docs.microsoft.com/azure/role-based-access-control/elevate-access-global-admin) to get access to the subscription.

## **Recommended documents**

- [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
- [Elevate access for a Global Administrator in Azure Active Directory](https://docs.microsoft.com/azure/role-based-access-control/elevate-access-global-admin)
