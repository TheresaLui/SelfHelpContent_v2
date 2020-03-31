<properties 
    pageTitle="What permissions are needed for Application Insights?"
    description="Explain what permissions are used in Application Insights"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_permissions"
    displayOrder="105"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax"
    productPesIds="15693" 
    supportTopicIds="32402604, 32602220"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# What permissions are needed for Application Insights?

## **Recommended Steps**

To control Application Insights resources and linked-resources such as **Web Tests** and **Alerts**, you must apply your permissions at the **resource group** level. This requires you to plan your resources properly to avoid granting access to a resource that is not expected.

### Permission to View Resource and Data

1. Add user to the **Reader** at the **resource group** or **component** level
2. Add user to the **Log Analytics Reader** at the **resource group** level

### Permission to Edit or Create Resources and View Data

1. Add user to the **Application Insights Component contributor** at the **resource group** level

### I need to do something custom

Application Insights has a number of built in roles to satisfy the most common scenarios. If you find that you need to do something custom you must create a [custom RBAC](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) role. Creation of this role is not supported by the Application Insights support team. Please work with the Azure Active Directory team to create this role.

## **Recommended Documents**

* [Roles Overview](https://docs.microsoft.com/azure/azure-monitor/app/resources-roles-access-control)
* [Built-in roles](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader)
