<properties
    pageTitle="Tools and management - IAM access control"
    description="Tools and management - IAM access control"
    service="microsoft.logicapps"
    resource="logicapps"
    authors="v-miegge"
    ms.author="kawilson"
    selfHelpType="generic"
    supportTopicIds="32742525"
    resourceTags=""
    productPesIds="15791"
    ownershipId="Compute_LogicApps"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ddff6120-251d-4669-8401-e9667b14fa28"
/>

# Tools and management - IAM access control

To access resources in other Azure Active Directory (Azure AD) tenants and authenticate your identity without signing in, your logic app can use a managed identity (formerly Managed Service Identity or MSI), rather than credentials or secrets. Azure manages this identity for you and helps secure your credentials because you don't have to provide or rotate secrets.

"Azure Logic Apps supports both system-assigned and user-assigned managed identities. Your logic app can use either the system-assigned identity or a single user-assigned identity, which you can share across a group of logic apps, but not both. Currently, only specific built-in triggers and actions support managed identities, not managed connectors or connections. These include the following:

- HTTP
- Azure Functions
- Azure API Management
- Azure App Services

## **Recommended Documents**

- [Prerequisites](https://docs.microsoft.com/azure/logic-apps/create-managed-service-identity#prerequisites)
- [Enable identity access to resources](https://docs.microsoft.com/azure/logic-apps/create-managed-service-identity)
- [Disable identity access from resources](https://docs.microsoft.com/azure/logic-apps/create-managed-service-identity)
