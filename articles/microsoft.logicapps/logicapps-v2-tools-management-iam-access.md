<properties
    pageTitle="Azure Logic Apps - IAM access control"
    description="Azure Logic Apps - IAM access control"
    service="microsoft.logicapps"
    resource="logicapps"
    authors="v-miegge"
    ms.author="kawilson"
    selfHelpType="generic"
    supportTopicIds="32780496"
    resourceTags=""
    productPesIds="17378"
    ownershipId="Compute_LogicApps"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fa5b2865-5a75-49f2-acff-e5b90ab29bc4"
/>

# Azure Logic Apps - IAM access control

To access resources in other Azure Active Directory (Azure AD) tenants and authenticate your identity without signing in, your logic app can use a managed identity (formerly Managed Service Identity or MSI), rather than credentials or secrets. Azure manages this identity for you and helps secure your credentials because you don't have to provide or rotate secrets.

Azure Logic Apps supports both system-assigned and user-assigned managed identities. Your logic app can use either the system-assigned identity or a single user-assigned identity, which you can share across a group of logic apps, but not both. Currently, only specific built-in triggers and actions support managed identities, not managed connectors or connections, for example:

- HTTP
- Azure Functions
- Azure API Management
- Azure App Services

## **Recommended Documents**

- [Prerequisites](https://docs.microsoft.com/azure/logic-apps/create-managed-service-identity#prerequisites)
- [Enable identity access to resources](https://docs.microsoft.com/azure/logic-apps/create-managed-service-identity)
