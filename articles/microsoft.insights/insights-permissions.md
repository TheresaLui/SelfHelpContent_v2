<properties 
    pageTitle="I need help with Role-Based Access Control (RBAC)"
    description="Explain what permissions are used in Application Insights"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_permissions"
    displayOrder="105"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32402604,32602220,32729593"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# I need help with Role-Based Access Control (RBAC)

## **Recommended Steps**

To control Application Insights resources and linked-resources such as **Web Tests** and **Alerts**, you must apply your permissions at the **resource group** level. This requires you to plan your resources properly to avoid granting access to a resource that is not expected.

### Permission to View Resource and Data

* Add user to the **Reader** role at the **resource group** or **component** level
* Add user to the **Monitoring Reader** role at the **resource group** level

### Permission to Edit or Create Resources and View Data

* Add user to the **Application Insights Component Contributor** or **Monitoring Contributor** role at the **resource group** level

### I can see data in Logs-based views (ex. Logs, Performance, Failures) but not Metrics data (ex. Overview)

* Ensure the user has **Reader** or **Monitoring Reader** access to the resource. Some more granular roles may grant access to the resource without granting Metrics data access.

### I need to do something custom

Application Insights has a number of built in roles to satisfy the most common scenarios. If you find that you need to do something custom you must create a [custom RBAC](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) role. Creation of this role is not supported by the Application Insights support team. Please work with the Azure Active Directory team to create this role.

## **Recommended Documents**

* [Roles Overview](https://docs.microsoft.com/azure/azure-monitor/app/resources-roles-access-control)
* [Built-in roles](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader)
