<properties
    pageTitle="Problems with custom roles"
    description="Azure Active Directory troubleshooting"
    infoBubbleText=""
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    displayOrder=""
    articleId=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32615422"
    resourceTags=""
    productPesIds="16578"​
    cloudEnvironments="public"
/>

# Problems with custom roles 

Choose this category for issues related to creating, reading, updating, or deleting custom roles in Azure RBAC.

**Role definition limit exceeded. No more role definitions can be created**

Azure supports up to 2000 custom roles in a tenant. [Learn more](https://docs.microsoft.com/azure/role-based-access-control/custom-roles)

**Unable to modify an existing custom role**

Check whether one or more assignable scopes have been deleted in the tenant. Currently, there is no self-service solution to address this issue. Create a support request.
