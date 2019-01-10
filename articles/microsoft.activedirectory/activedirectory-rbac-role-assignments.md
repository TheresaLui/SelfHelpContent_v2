<properties
    pageTitle="Problems with RBAC role assignments"
    description="Azure Active Directory troubleshooting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="rolyon"
    ms.author="rolyon"
    displayOrder=""
    articleId=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32615426"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public"
/>

# Problems with RBAC role assignments

## **Recommended Steps**

* If you are unable to add a role assignment because the **Add role assignment** option is disabled or because you get a permissions error, check that you are using a role that has the Microsoft.Authorization/roleAssignments/write permission at the scope you are trying to assign the role. If you don't have this permission, check with your subscription administrator.
* If you get a permissions error when you try to create a resource, check that you are using a role that has write permission to the resource at the selected scope. If you don't have write permission, check with your subscription administrator.
* If you get a permissions error when you try to create or update a support ticket, check that you are using a role that has the Microsoft.Support/* permission, such as Support Request Contributor.
* If you get an error that the number of role assignments are exceeded when you try to assign a role, try to reduce the number of role assignments by assigning roles to groups instead. Azure supports up to 2000 role assignments per subscription.

## **Recommended Documents**

- [Manage access using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)
- [Built-in roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
